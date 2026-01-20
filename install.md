curl --proto '=https' --tlsv1.2 -sSf \
"https://desktop-release.q.us-east-1.amazonaws.com/latest/q-x86_64-linux.zip" \
-o "q.zip"

unzip q.zip
./q/install.sh




sudo apt-get update
sudo apt install libfuse2

curl --proto '=https' --tlsv1.2 -sSf \
https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.deb \
-o amazon-q.deb

sudo apt install -y ./amazon-q.deb


brew install uvx
sudo snap install astral-uvx --classic



-- mcp configuration --   
{
  "mcpServers": {
    "awslabs.cdk-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.cdk-mcp-server@latest"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      }
    },
    "awslabs.aws-diagram-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.aws-diagram-mcp-server"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "autoApprove": [],
      "disabled": false
    }
  }
}
-- mcp configuration --



