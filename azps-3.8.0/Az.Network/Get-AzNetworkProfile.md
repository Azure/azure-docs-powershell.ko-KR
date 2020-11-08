---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043318"
---
# <span data-ttu-id="33b74-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="33b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33b74-102">SYNOPSIS</span></span>
<span data-ttu-id="33b74-103">기존 네트워크 프로필 최상위 수준 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="33b74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33b74-104">SYNTAX</span></span>

### <span data-ttu-id="33b74-105">GetByResourceNameNoExpandParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="33b74-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33b74-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b74-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33b74-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b74-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33b74-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b74-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b74-109">설명은</span><span class="sxs-lookup"><span data-stu-id="33b74-109">DESCRIPTION</span></span>
<span data-ttu-id="33b74-110">**AzNetworkProfile** cmdlet은 기존 네트워크 프로필의 상위 수준 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="33b74-111">예제의</span><span class="sxs-lookup"><span data-stu-id="33b74-111">EXAMPLES</span></span>

### <span data-ttu-id="33b74-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="33b74-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="33b74-113">이렇게 하면 리소스 그룹 rg1에서 네트워크 프로필 np1 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="33b74-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="33b74-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="33b74-115">"Np"로 시작 하는 네트워크 프로필을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="33b74-116">변수</span><span class="sxs-lookup"><span data-stu-id="33b74-116">PARAMETERS</span></span>

### <span data-ttu-id="33b74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-117">-DefaultProfile</span></span>
<span data-ttu-id="33b74-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b74-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="33b74-119">-ExpandResource</span></span>
<span data-ttu-id="33b74-120">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b74-121">-이름</span><span class="sxs-lookup"><span data-stu-id="33b74-121">-Name</span></span>
<span data-ttu-id="33b74-122">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="33b74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b74-123">-ResourceGroupName</span></span>
<span data-ttu-id="33b74-124">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="33b74-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33b74-125">-ResourceId</span></span>
<span data-ttu-id="33b74-126">네트워크 프로필의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b74-127">CommonParameters</span></span>
<span data-ttu-id="33b74-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33b74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b74-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33b74-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b74-130">입력</span><span class="sxs-lookup"><span data-stu-id="33b74-130">INPUTS</span></span>

### <span data-ttu-id="33b74-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33b74-131">System.String</span></span>

## <span data-ttu-id="33b74-132">출력</span><span class="sxs-lookup"><span data-stu-id="33b74-132">OUTPUTS</span></span>

### <span data-ttu-id="33b74-133">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="33b74-134">상속자</span><span class="sxs-lookup"><span data-stu-id="33b74-134">NOTES</span></span>

## <span data-ttu-id="33b74-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33b74-135">RELATED LINKS</span></span>

[<span data-ttu-id="33b74-136">새로운 AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="33b74-137">제거-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="33b74-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33b74-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)