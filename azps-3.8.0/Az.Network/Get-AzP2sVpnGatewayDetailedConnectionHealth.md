---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033825"
---
# <span data-ttu-id="20c74-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="20c74-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="20c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c74-102">SYNOPSIS</span></span>
<span data-ttu-id="20c74-103">P2SVpnGateway에서 현재 지점의 사이트 연결에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="20c74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20c74-104">SYNTAX</span></span>

### <span data-ttu-id="20c74-105">ByP2SVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="20c74-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20c74-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="20c74-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c74-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="20c74-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c74-108">설명은</span><span class="sxs-lookup"><span data-stu-id="20c74-108">DESCRIPTION</span></span>
<span data-ttu-id="20c74-109">**AzP2sVpnGatewayDetailedConnectionHealth** cmdlet을 사용 하면 P2SVpnGateway에서 현재 지점의 사이트 연결에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="20c74-110">이 자세한 상태 정보를 저장할 수 있는 SAS url을 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="20c74-111">예제의</span><span class="sxs-lookup"><span data-stu-id="20c74-111">EXAMPLES</span></span>

### <span data-ttu-id="20c74-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="20c74-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="20c74-113">**AzP2sVpnGatewayDetailedConnectionHealth** cmdlet을 사용 하면 P2SVpnGateway에서 현재 지점의 사이트 연결에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="20c74-114">고객이 통과 한 SAS url 다운로드에서 상태 세부 정보를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="20c74-115">여기에는 사용자 이름, 바이트 수, 바이트 출력, 할당 된 ip 주소 등과 같은 사이트 연결에 대 한 각 지점의 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="20c74-116">변수</span><span class="sxs-lookup"><span data-stu-id="20c74-116">PARAMETERS</span></span>

### <span data-ttu-id="20c74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c74-117">-DefaultProfile</span></span>
<span data-ttu-id="20c74-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c74-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20c74-119">-InputObject</span></span>
<span data-ttu-id="20c74-120">수정할 p2s vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="20c74-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="20c74-121">-이름</span><span class="sxs-lookup"><span data-stu-id="20c74-121">-Name</span></span>
<span data-ttu-id="20c74-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-122">The resource name.</span></span>

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

### <span data-ttu-id="20c74-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="20c74-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="20c74-124">P2s vpn 연결 상태가 기록 될 OutputBlob Sas url입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="20c74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c74-125">-ResourceGroupName</span></span>
<span data-ttu-id="20c74-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-126">The resource group name.</span></span>

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

### <span data-ttu-id="20c74-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c74-127">-ResourceId</span></span>
<span data-ttu-id="20c74-128">수정할 P2SVpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="20c74-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="20c74-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="20c74-130">필터링 할 P2S vpn 사용자 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="20c74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c74-131">CommonParameters</span></span>
<span data-ttu-id="20c74-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c74-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c74-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c74-134">입력</span><span class="sxs-lookup"><span data-stu-id="20c74-134">INPUTS</span></span>

### <span data-ttu-id="20c74-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20c74-135">System.String</span></span>
<span data-ttu-id="20c74-136">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="20c74-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="20c74-137">출력</span><span class="sxs-lookup"><span data-stu-id="20c74-137">OUTPUTS</span></span>

### <span data-ttu-id="20c74-138">PSP2SVpnConnectionHealth에 대 한.</span><span class="sxs-lookup"><span data-stu-id="20c74-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="20c74-139">상속자</span><span class="sxs-lookup"><span data-stu-id="20c74-139">NOTES</span></span>

## <span data-ttu-id="20c74-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20c74-140">RELATED LINKS</span></span>
