---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187129"
---
# <span data-ttu-id="ecc64-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="ecc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc64-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc64-103">기존 네트워크 프로필 최상위 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="ecc64-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecc64-104">SYNTAX</span></span>

### <span data-ttu-id="ecc64-105">GetByResourceNameNoExpandParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ecc64-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecc64-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc64-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecc64-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc64-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecc64-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecc64-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc64-109">설명</span><span class="sxs-lookup"><span data-stu-id="ecc64-109">DESCRIPTION</span></span>
<span data-ttu-id="ecc64-110">**Get-AzNetworkProfile** cmdlet은 기존 네트워크 프로필 최상위 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="ecc64-111">예제</span><span class="sxs-lookup"><span data-stu-id="ecc64-111">EXAMPLES</span></span>

### <span data-ttu-id="ecc64-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecc64-112">Example 1</span></span>
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

<span data-ttu-id="ecc64-113">리소스 그룹 rg1에서 np1 네트워크 프로필을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="ecc64-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ecc64-114">Example 2</span></span>
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

<span data-ttu-id="ecc64-115">"np"로 시작하는 네트워크 프로필을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="ecc64-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc64-116">PARAMETERS</span></span>

### <span data-ttu-id="ecc64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-117">-DefaultProfile</span></span>
<span data-ttu-id="ecc64-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc64-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ecc64-119">-ExpandResource</span></span>
<span data-ttu-id="ecc64-120">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-120">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ecc64-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ecc64-121">-Name</span></span>
<span data-ttu-id="ecc64-122">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="ecc64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc64-123">-ResourceGroupName</span></span>
<span data-ttu-id="ecc64-124">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="ecc64-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc64-125">-ResourceId</span></span>
<span data-ttu-id="ecc64-126">네트워크 프로필의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-126">The Azure resource manager id of the network profile.</span></span>

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

### <span data-ttu-id="ecc64-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc64-127">CommonParameters</span></span>
<span data-ttu-id="ecc64-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc64-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc64-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecc64-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc64-130">입력</span><span class="sxs-lookup"><span data-stu-id="ecc64-130">INPUTS</span></span>

### <span data-ttu-id="ecc64-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ecc64-131">System.String</span></span>

## <span data-ttu-id="ecc64-132">출력</span><span class="sxs-lookup"><span data-stu-id="ecc64-132">OUTPUTS</span></span>

### <span data-ttu-id="ecc64-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ecc64-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecc64-134">NOTES</span></span>

## <span data-ttu-id="ecc64-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecc64-135">RELATED LINKS</span></span>

[<span data-ttu-id="ecc64-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="ecc64-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="ecc64-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecc64-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
