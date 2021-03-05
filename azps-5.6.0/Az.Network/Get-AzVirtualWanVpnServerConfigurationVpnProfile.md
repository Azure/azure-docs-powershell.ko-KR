---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: e0a39aac53b13356eb9719cad6e2ade11483cfe7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982459"
---
# <span data-ttu-id="13d87-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="13d87-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="13d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13d87-102">SYNOPSIS</span></span>
<span data-ttu-id="13d87-103">지점 및 사이트 클라이언트 설정에 대한 VirtualWan-VpnServerConfiguration 수준에서 Vpn 프로필을 생성하고 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="13d87-104">구문</span><span class="sxs-lookup"><span data-stu-id="13d87-104">SYNTAX</span></span>

### <span data-ttu-id="13d87-105">ByVirtualWanNameByVpnServerConfigurationObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="13d87-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="13d87-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d87-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="13d87-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="13d87-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d87-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="13d87-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d87-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="13d87-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d87-111">설명</span><span class="sxs-lookup"><span data-stu-id="13d87-111">DESCRIPTION</span></span>
<span data-ttu-id="13d87-112">**Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet을 사용하면 사이트 지점 클라이언트 설정에 대한 VirtualWan-VpnServerConfiguration 수준에서 Vpn 프로필을 생성하고 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="13d87-113">지점 및 사이트 클라이언트에서 Azure P2SVpnGateway로 지점 및 사이트 연결에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="13d87-114">예제</span><span class="sxs-lookup"><span data-stu-id="13d87-114">EXAMPLES</span></span>

### <span data-ttu-id="13d87-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="13d87-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="13d87-116">위의 명령은 고객에 대한 SAS URL을 생성하고 반환하여 지점 및 사이트 클라이언트 VirtualWan-VpnServerConfiguration 수준으로 VPN 프로필을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="13d87-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13d87-117">PARAMETERS</span></span>

### <span data-ttu-id="13d87-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="13d87-118">-AuthenticationMethod</span></span>
<span data-ttu-id="13d87-119">인증 방법</span><span class="sxs-lookup"><span data-stu-id="13d87-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d87-120">-DefaultProfile</span></span>
<span data-ttu-id="13d87-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d87-122">-Name</span><span class="sxs-lookup"><span data-stu-id="13d87-122">-Name</span></span>
<span data-ttu-id="13d87-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d87-124">-ResourceGroupName</span></span>
<span data-ttu-id="13d87-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d87-126">-ResourceId</span></span>
<span data-ttu-id="13d87-127">가상 wan에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="13d87-128">-VirtualWanObject</span></span>
<span data-ttu-id="13d87-129">가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="13d87-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="13d87-131">이 VirtualWan이 연결된 VpnServerConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="13d87-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="13d87-133">이 Virtual wan이 연결되는 Vpn 서버 구성 개체의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13d87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d87-134">CommonParameters</span></span>
<span data-ttu-id="13d87-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13d87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d87-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13d87-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d87-137">입력</span><span class="sxs-lookup"><span data-stu-id="13d87-137">INPUTS</span></span>

### <span data-ttu-id="13d87-138">System.String</span><span class="sxs-lookup"><span data-stu-id="13d87-138">System.String</span></span>
<span data-ttu-id="13d87-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="13d87-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="13d87-140">출력</span><span class="sxs-lookup"><span data-stu-id="13d87-140">OUTPUTS</span></span>

### <span data-ttu-id="13d87-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="13d87-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="13d87-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13d87-142">NOTES</span></span>

## <span data-ttu-id="13d87-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13d87-143">RELATED LINKS</span></span>
