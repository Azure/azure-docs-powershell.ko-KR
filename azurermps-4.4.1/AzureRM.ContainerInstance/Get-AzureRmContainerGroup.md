---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: f97f7ca82ae17c61994a84fbc4b1405b41fdb566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537843"
---
# <span data-ttu-id="4cd72-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4cd72-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="4cd72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd72-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd72-103">컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cd72-104">SYNTAX</span></span>

### <span data-ttu-id="4cd72-105">ListContainerGroupParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cd72-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cd72-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="4cd72-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cd72-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4cd72-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cd72-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4cd72-108">DESCRIPTION</span></span>
<span data-ttu-id="4cd72-109">**AzureRmContainerGroup** cmdlet은 지정 된 컨테이너 그룹 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="4cd72-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4cd72-110">EXAMPLES</span></span>

### <span data-ttu-id="4cd72-111">예제 1: 지정 된 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-111">Example 1: Gets a specified container group</span></span>
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
```

<span data-ttu-id="4cd72-112">명령에서 지정 된 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="4cd72-113">예제 2: 리소스 그룹의 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="4cd72-114">명령은 리소스 그룹의 컨테이너 그룹을 가져옵니다 `demo` .</span><span class="sxs-lookup"><span data-stu-id="4cd72-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="4cd72-115">예제 3: 현재 구독의 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="4cd72-116">명령이 현재 구독에서 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="4cd72-117">예제 4: 리소스 Id를 사용 하 여 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-117">Example 4: Gets container groups using resource Id.</span></span>
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
```

<span data-ttu-id="4cd72-118">명령이 리소스 Id를 사용 하 여 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="4cd72-119">변수</span><span class="sxs-lookup"><span data-stu-id="4cd72-119">PARAMETERS</span></span>

### <span data-ttu-id="4cd72-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4cd72-120">-Name</span></span>
<span data-ttu-id="4cd72-121">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-121">The container group Name.</span></span>

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

### <span data-ttu-id="4cd72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd72-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cd72-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="4cd72-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cd72-124">-ResourceId</span></span>
<span data-ttu-id="4cd72-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-125">The resource id.</span></span>

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

### <span data-ttu-id="4cd72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd72-126">-DefaultProfile</span></span>
<span data-ttu-id="4cd72-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd72-128">CommonParameters</span></span>
<span data-ttu-id="4cd72-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd72-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd72-131">입력</span><span class="sxs-lookup"><span data-stu-id="4cd72-131">INPUTS</span></span>

### <span data-ttu-id="4cd72-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4cd72-132">System.String</span></span>

## <span data-ttu-id="4cd72-133">출력</span><span class="sxs-lookup"><span data-stu-id="4cd72-133">OUTPUTS</span></span>

### <span data-ttu-id="4cd72-134">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="4cd72-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4cd72-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4cd72-135">NOTES</span></span>

## <span data-ttu-id="4cd72-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cd72-136">RELATED LINKS</span></span>

