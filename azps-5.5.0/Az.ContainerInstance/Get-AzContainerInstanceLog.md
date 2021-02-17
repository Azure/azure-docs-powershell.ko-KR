---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177380"
---
# <span data-ttu-id="67747-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="67747-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="67747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67747-102">SYNOPSIS</span></span>
<span data-ttu-id="67747-103">컨테이너 그룹의 컨테이너 인스턴스 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="67747-104">구문</span><span class="sxs-lookup"><span data-stu-id="67747-104">SYNTAX</span></span>

### <span data-ttu-id="67747-105">GetContainerInstanceLogByNamesParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="67747-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67747-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="67747-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67747-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="67747-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67747-108">설명</span><span class="sxs-lookup"><span data-stu-id="67747-108">DESCRIPTION</span></span>
<span data-ttu-id="67747-109">**Get-AzContainerInstanceLog** cmdlet은 컨테이너 그룹의 컨테이너 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="67747-110">예제</span><span class="sxs-lookup"><span data-stu-id="67747-110">EXAMPLES</span></span>

### <span data-ttu-id="67747-111">예제 1: 컨테이너 인스턴스의 테일 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="67747-112">컨테이너 그룹에서 `container1` 로그를 `mycontainer` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="67747-113">기본적으로 최대 4MB 로그 콘텐츠를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="67747-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="67747-114">예제 2: 컨테이너 그룹과 이름이 같은 컨테이너 인스턴스의 테일 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="67747-115">컨테이너 그룹에서 `mycontainer` 로그를 `mycontainer` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="67747-116">기본적으로 최대 4MB 로그 콘텐츠를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="67747-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="67747-117">예제 3: 컨테이너 인스턴스의 로그의 테일 2줄을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="67747-118">컨테이너 그룹에서 로그의 테일 2 `container1` 줄을 `mycontainer` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="67747-119">예제 4: 컨테이너 그룹의 파이프된 컨테이너 인스턴스의 테일 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="67747-120">컨테이너 그룹에서 `mycontainer` 파이프된 로그를 `mycontainer` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67747-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="67747-121">기본적으로 최대 4MB 로그 콘텐츠를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="67747-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="67747-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67747-122">PARAMETERS</span></span>

### <span data-ttu-id="67747-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="67747-123">-ContainerGroupName</span></span>
<span data-ttu-id="67747-124">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67747-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67747-125">-DefaultProfile</span></span>
<span data-ttu-id="67747-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67747-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="67747-127">-InputContainerGroup</span></span>
<span data-ttu-id="67747-128">입력 컨테이너 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67747-129">-Name</span><span class="sxs-lookup"><span data-stu-id="67747-129">-Name</span></span>
<span data-ttu-id="67747-130">컨테이너 그룹의 컨테이너 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-130">The container instance name in the container group.</span></span>
<span data-ttu-id="67747-131">기본값: 컨테이너 그룹 이름과 동일</span><span class="sxs-lookup"><span data-stu-id="67747-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67747-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67747-132">-ResourceGroupName</span></span>
<span data-ttu-id="67747-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67747-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67747-134">-ResourceId</span></span>
<span data-ttu-id="67747-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67747-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="67747-136">-Tail</span></span>
<span data-ttu-id="67747-137">로그에서 끝까지의 줄 수입니다.</span><span class="sxs-lookup"><span data-stu-id="67747-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="67747-138">지정하지 않으면 cmdlet은 최대 4MB 꼬리 로그를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="67747-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67747-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67747-139">CommonParameters</span></span>
<span data-ttu-id="67747-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67747-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67747-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67747-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67747-142">입력</span><span class="sxs-lookup"><span data-stu-id="67747-142">INPUTS</span></span>

### <span data-ttu-id="67747-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="67747-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="67747-144">System.String</span><span class="sxs-lookup"><span data-stu-id="67747-144">System.String</span></span>

## <span data-ttu-id="67747-145">출력</span><span class="sxs-lookup"><span data-stu-id="67747-145">OUTPUTS</span></span>

### <span data-ttu-id="67747-146">System.String</span><span class="sxs-lookup"><span data-stu-id="67747-146">System.String</span></span>

## <span data-ttu-id="67747-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67747-147">NOTES</span></span>

## <span data-ttu-id="67747-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67747-148">RELATED LINKS</span></span>
