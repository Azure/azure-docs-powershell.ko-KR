---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: f046b9a57f0827977927e31d5009c6276cd89279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697141"
---
# <span data-ttu-id="b1706-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="b1706-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="b1706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1706-102">SYNOPSIS</span></span>
<span data-ttu-id="b1706-103">컨테이너 그룹에서 컨테이너 인스턴스의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="b1706-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1706-104">SYNTAX</span></span>

### <span data-ttu-id="b1706-105">GetContainerInstanceLogByNamesParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1706-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1706-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b1706-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1706-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b1706-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1706-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b1706-108">DESCRIPTION</span></span>
<span data-ttu-id="b1706-109">**Get-AzContainerInstanceLog** cmdlet은 컨테이너 그룹의 컨테이너에 대 한 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="b1706-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b1706-110">EXAMPLES</span></span>

### <span data-ttu-id="b1706-111">예제 1: 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1706-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="b1706-112">컨테이너 그룹에서 로그를 가져옵니다 `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="b1706-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="b1706-113">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="b1706-114">예제 2: 컨테이너 그룹과 동일한 이름을 가진 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1706-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="b1706-115">컨테이너 그룹에서 로그를 가져옵니다 `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="b1706-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="b1706-116">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="b1706-117">예제 3: 컨테이너 인스턴스의 로그에 대 한 꼬리 2 줄 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1706-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="b1706-118">컨테이너 그룹에서 log의 꼬리 2 줄을 가져옵니다 `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="b1706-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="b1706-119">예제 4: 컨테이너의 파이프라인 그룹에서 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1706-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="b1706-120">컨테이너 그룹의 파이프에서 로그를 가져옵니다 `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="b1706-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="b1706-121">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="b1706-122">변수</span><span class="sxs-lookup"><span data-stu-id="b1706-122">PARAMETERS</span></span>

### <span data-ttu-id="b1706-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="b1706-123">-ContainerGroupName</span></span>
<span data-ttu-id="b1706-124">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-124">The container group name.</span></span>

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

### <span data-ttu-id="b1706-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1706-125">-DefaultProfile</span></span>
<span data-ttu-id="b1706-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1706-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b1706-127">-InputContainerGroup</span></span>
<span data-ttu-id="b1706-128">입력 컨테이너 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-128">The input container group object.</span></span>

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

### <span data-ttu-id="b1706-129">-이름</span><span class="sxs-lookup"><span data-stu-id="b1706-129">-Name</span></span>
<span data-ttu-id="b1706-130">컨테이너 그룹의 컨테이너 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-130">The container instance name in the container group.</span></span>
<span data-ttu-id="b1706-131">Default: 컨테이너 그룹 이름과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="b1706-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1706-132">-ResourceGroupName</span></span>
<span data-ttu-id="b1706-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-133">The resource group name.</span></span>

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

### <span data-ttu-id="b1706-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1706-134">-ResourceId</span></span>
<span data-ttu-id="b1706-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-135">The resource id.</span></span>

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

### <span data-ttu-id="b1706-136">-꼬리</span><span class="sxs-lookup"><span data-stu-id="b1706-136">-Tail</span></span>
<span data-ttu-id="b1706-137">로그의 꼬리에 대 한 줄 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="b1706-138">지정 하지 않으면 cmdlet이 최대 4MB의 단측 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="b1706-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1706-139">CommonParameters</span></span>
<span data-ttu-id="b1706-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1706-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1706-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1706-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1706-142">입력</span><span class="sxs-lookup"><span data-stu-id="b1706-142">INPUTS</span></span>

### <span data-ttu-id="b1706-143">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="b1706-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="b1706-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1706-144">System.String</span></span>

## <span data-ttu-id="b1706-145">출력</span><span class="sxs-lookup"><span data-stu-id="b1706-145">OUTPUTS</span></span>

### <span data-ttu-id="b1706-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1706-146">System.String</span></span>

## <span data-ttu-id="b1706-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b1706-147">NOTES</span></span>

## <span data-ttu-id="b1706-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1706-148">RELATED LINKS</span></span>
