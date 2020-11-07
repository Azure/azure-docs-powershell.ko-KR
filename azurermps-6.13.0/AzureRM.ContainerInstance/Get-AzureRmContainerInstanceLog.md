---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 08a4ab0f0d937f06ee0ac958aa57a2f0eed5e4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701978"
---
# <span data-ttu-id="7e363-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="7e363-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="7e363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e363-102">SYNOPSIS</span></span>
<span data-ttu-id="7e363-103">컨테이너 그룹에서 컨테이너 인스턴스의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e363-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e363-104">SYNTAX</span></span>

### <span data-ttu-id="7e363-105">GetContainerInstanceLogByNamesParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e363-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e363-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7e363-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e363-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7e363-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e363-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7e363-108">DESCRIPTION</span></span>
<span data-ttu-id="7e363-109">**Get-AzureRmContainerInstanceLog** cmdlet은 컨테이너 그룹의 컨테이너에 대 한 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="7e363-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7e363-110">EXAMPLES</span></span>

### <span data-ttu-id="7e363-111">예제 1: 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e363-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e363-112">컨테이너 그룹에서 로그를 가져옵니다 `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e363-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="7e363-113">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="7e363-114">예제 2: 컨테이너 그룹과 동일한 이름을 가진 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e363-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e363-115">컨테이너 그룹에서 로그를 가져옵니다 `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e363-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="7e363-116">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="7e363-117">예제 3: 컨테이너 인스턴스의 로그에 대 한 꼬리 2 줄 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e363-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="7e363-118">컨테이너 그룹에서 log의 꼬리 2 줄을 가져옵니다 `container1` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e363-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="7e363-119">예제 4: 컨테이너의 파이프라인 그룹에서 컨테이너 인스턴스의 꼬리 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e363-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="7e363-120">컨테이너 그룹의 파이프에서 로그를 가져옵니다 `mycontainer` `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="7e363-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="7e363-121">기본적으로이 파일은 최대 4MB의 로그 콘텐츠를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="7e363-122">변수</span><span class="sxs-lookup"><span data-stu-id="7e363-122">PARAMETERS</span></span>

### <span data-ttu-id="7e363-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="7e363-123">-ContainerGroupName</span></span>
<span data-ttu-id="7e363-124">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-124">The container group name.</span></span>

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

### <span data-ttu-id="7e363-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e363-125">-DefaultProfile</span></span>
<span data-ttu-id="7e363-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e363-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7e363-127">-InputContainerGroup</span></span>
<span data-ttu-id="7e363-128">입력 컨테이너 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-128">The input container group object.</span></span>

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

### <span data-ttu-id="7e363-129">-이름</span><span class="sxs-lookup"><span data-stu-id="7e363-129">-Name</span></span>
<span data-ttu-id="7e363-130">컨테이너 그룹의 컨테이너 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-130">The container instance name in the container group.</span></span>
<span data-ttu-id="7e363-131">Default: 컨테이너 그룹 이름과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="7e363-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e363-132">-ResourceGroupName</span></span>
<span data-ttu-id="7e363-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-133">The resource group name.</span></span>

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

### <span data-ttu-id="7e363-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e363-134">-ResourceId</span></span>
<span data-ttu-id="7e363-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-135">The resource id.</span></span>

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

### <span data-ttu-id="7e363-136">-꼬리</span><span class="sxs-lookup"><span data-stu-id="7e363-136">-Tail</span></span>
<span data-ttu-id="7e363-137">로그의 꼬리에 대 한 줄 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="7e363-138">지정 하지 않으면 cmdlet이 최대 4MB의 단측 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="7e363-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e363-139">CommonParameters</span></span>
<span data-ttu-id="7e363-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e363-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e363-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e363-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e363-142">입력</span><span class="sxs-lookup"><span data-stu-id="7e363-142">INPUTS</span></span>

### <span data-ttu-id="7e363-143">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="7e363-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="7e363-144">매개 변수: InputContainerGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e363-144">Parameters: InputContainerGroup (ByValue)</span></span>

### <span data-ttu-id="7e363-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e363-145">System.String</span></span>

## <span data-ttu-id="7e363-146">출력</span><span class="sxs-lookup"><span data-stu-id="7e363-146">OUTPUTS</span></span>

### <span data-ttu-id="7e363-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e363-147">System.String</span></span>

## <span data-ttu-id="7e363-148">상속자</span><span class="sxs-lookup"><span data-stu-id="7e363-148">NOTES</span></span>

## <span data-ttu-id="7e363-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e363-149">RELATED LINKS</span></span>
