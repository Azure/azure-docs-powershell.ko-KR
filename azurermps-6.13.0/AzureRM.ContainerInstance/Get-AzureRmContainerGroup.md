---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: b2107a667fe3d00ec0b6e9180b2edc99e864445c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524520"
---
# <span data-ttu-id="60187-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="60187-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="60187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60187-102">SYNOPSIS</span></span>
<span data-ttu-id="60187-103">컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60187-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60187-104">SYNTAX</span></span>

### <span data-ttu-id="60187-105">ListContainerGroupParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="60187-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60187-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="60187-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60187-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="60187-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60187-108">설명은</span><span class="sxs-lookup"><span data-stu-id="60187-108">DESCRIPTION</span></span>
<span data-ttu-id="60187-109">**AzureRmContainerGroup** cmdlet은 지정 된 컨테이너 그룹 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="60187-110">예제의</span><span class="sxs-lookup"><span data-stu-id="60187-110">EXAMPLES</span></span>

### <span data-ttu-id="60187-111">예제 1: 지정 된 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="60187-112">명령에서 지정 된 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="60187-113">예제 2: 리소스 그룹의 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="60187-114">명령은 리소스 그룹의 컨테이너 그룹을 가져옵니다 `demo` .</span><span class="sxs-lookup"><span data-stu-id="60187-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="60187-115">예제 3: 현재 구독의 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="60187-116">명령이 현재 구독에서 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="60187-117">예제 4: 리소스 Id를 사용 하 여 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="60187-118">명령이 리소스 Id를 사용 하 여 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60187-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="60187-119">변수</span><span class="sxs-lookup"><span data-stu-id="60187-119">PARAMETERS</span></span>

### <span data-ttu-id="60187-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60187-120">-DefaultProfile</span></span>
<span data-ttu-id="60187-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60187-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60187-122">-이름</span><span class="sxs-lookup"><span data-stu-id="60187-122">-Name</span></span>
<span data-ttu-id="60187-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60187-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60187-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60187-124">-ResourceGroupName</span></span>
<span data-ttu-id="60187-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60187-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60187-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60187-126">-ResourceId</span></span>
<span data-ttu-id="60187-127">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="60187-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60187-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60187-128">CommonParameters</span></span>
<span data-ttu-id="60187-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60187-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60187-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60187-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60187-131">입력</span><span class="sxs-lookup"><span data-stu-id="60187-131">INPUTS</span></span>

### <span data-ttu-id="60187-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60187-132">System.String</span></span>

## <span data-ttu-id="60187-133">출력</span><span class="sxs-lookup"><span data-stu-id="60187-133">OUTPUTS</span></span>

### <span data-ttu-id="60187-134">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="60187-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="60187-135">상속자</span><span class="sxs-lookup"><span data-stu-id="60187-135">NOTES</span></span>

## <span data-ttu-id="60187-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60187-136">RELATED LINKS</span></span>