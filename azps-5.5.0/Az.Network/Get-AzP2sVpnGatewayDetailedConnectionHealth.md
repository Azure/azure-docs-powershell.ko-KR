---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193772"
---
# <span data-ttu-id="24af6-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="24af6-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="24af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24af6-102">SYNOPSIS</span></span>
<span data-ttu-id="24af6-103">P2SVpnGateway에서 현재 지점과 사이트 연결에 대한 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="24af6-104">구문</span><span class="sxs-lookup"><span data-stu-id="24af6-104">SYNTAX</span></span>

### <span data-ttu-id="24af6-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="24af6-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24af6-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="24af6-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24af6-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="24af6-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24af6-108">설명</span><span class="sxs-lookup"><span data-stu-id="24af6-108">DESCRIPTION</span></span>
<span data-ttu-id="24af6-109">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet을 사용하면 P2SVpnGateway에서 현재 지점과 사이트 간 연결에 대한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="24af6-110">고객은 이 자세한 상태 정보를 입력할 수 있는 SAS URL을 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="24af6-111">예제</span><span class="sxs-lookup"><span data-stu-id="24af6-111">EXAMPLES</span></span>

### <span data-ttu-id="24af6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="24af6-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="24af6-113">**Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet을 사용하면 P2SVpnGateway에서 현재 지점과 사이트 간 연결에 대한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="24af6-114">고객은 전달된 SAS URL 다운로드에서 상태 세부 정보를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="24af6-115">사용자 이름, byte in, byte out, 할당된 IP 주소 등을 사용하여 각 지점과 사이트 연결에 대한 정보를 보여 주게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="24af6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24af6-116">PARAMETERS</span></span>

### <span data-ttu-id="24af6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24af6-117">-DefaultProfile</span></span>
<span data-ttu-id="24af6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24af6-119">-InputObject</span></span>
<span data-ttu-id="24af6-120">수정할 p2s vpn Gateway 개체</span><span class="sxs-lookup"><span data-stu-id="24af6-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24af6-121">-Name</span></span>
<span data-ttu-id="24af6-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="24af6-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="24af6-124">p2s vpn 연결 상태 기록할 OutputBlob Sas URL입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24af6-125">-ResourceGroupName</span></span>
<span data-ttu-id="24af6-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24af6-127">-ResourceId</span></span>
<span data-ttu-id="24af6-128">수정할 P2SVpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="24af6-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="24af6-130">필터링할 P2S vpn 사용자 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24af6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24af6-131">CommonParameters</span></span>
<span data-ttu-id="24af6-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24af6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24af6-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="24af6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24af6-134">입력</span><span class="sxs-lookup"><span data-stu-id="24af6-134">INPUTS</span></span>

### <span data-ttu-id="24af6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="24af6-135">System.String</span></span>
<span data-ttu-id="24af6-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="24af6-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="24af6-137">출력</span><span class="sxs-lookup"><span data-stu-id="24af6-137">OUTPUTS</span></span>

### <span data-ttu-id="24af6-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="24af6-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="24af6-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24af6-139">NOTES</span></span>

## <span data-ttu-id="24af6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24af6-140">RELATED LINKS</span></span>
