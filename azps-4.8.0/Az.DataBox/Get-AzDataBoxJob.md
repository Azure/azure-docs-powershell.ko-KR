---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056448"
---
# <span data-ttu-id="dc99b-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="dc99b-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="dc99b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc99b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc99b-103">Databox 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="dc99b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc99b-104">SYNTAX</span></span>

### <span data-ttu-id="dc99b-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc99b-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc99b-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc99b-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc99b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc99b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc99b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc99b-108">DESCRIPTION</span></span>
<span data-ttu-id="dc99b-109">**AzDataBoxJobs** Cmdlet은 Azure 구독에서 databox 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="dc99b-110">리소스 그룹을 지정 하는 경우이 cmdlet은 해당 리소스 그룹의 모든 databox 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="dc99b-111">리소스 그룹 이름과 함께 작업의 이름을 지정 하는 경우이 cmdlet은 해당 특정 databox 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="dc99b-112">구독 id 이외의 다른 값을 지정 하지 않으면이 cmdlet은 해당 구독에 속하는 모든 databox 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="dc99b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="dc99b-113">EXAMPLES</span></span>

### <span data-ttu-id="dc99b-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc99b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="dc99b-115">매개 변수가 없는 Get-AzDataBoxJob 구독 하는 모든 databox 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="dc99b-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="dc99b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="dc99b-117">ResourceGroupName 매개 변수가 있는 Get-AzDataBoxJob 지정 된 리소스 그룹 아래의 모든 databox 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="dc99b-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="dc99b-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="dc99b-119">ResourceGroupName 및 Name으로 지정 된 Get-AzDataBoxJob는 특정 databox 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="dc99b-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="dc99b-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="dc99b-121">ResourceId가 지정 된 Get-AzDataBoxJob는 특정 databox 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="dc99b-122">변수</span><span class="sxs-lookup"><span data-stu-id="dc99b-122">PARAMETERS</span></span>

### <span data-ttu-id="dc99b-123">-중단 됨</span><span class="sxs-lookup"><span data-stu-id="dc99b-123">-Aborted</span></span>
<span data-ttu-id="dc99b-124">중단 작업을 가져오는 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc99b-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-125">-취소 됨</span><span class="sxs-lookup"><span data-stu-id="dc99b-125">-Cancelled</span></span>
<span data-ttu-id="dc99b-126">취소 한 작업을 가져오는 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc99b-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-127">-완료 됨</span><span class="sxs-lookup"><span data-stu-id="dc99b-127">-Completed</span></span>
<span data-ttu-id="dc99b-128">완료 된 작업을 가져오는 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc99b-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="dc99b-129">-CompletedWithError</span></span>
<span data-ttu-id="dc99b-130">작업을 가져오는 스위치 매개 변수가 오류로 완료 됨</span><span class="sxs-lookup"><span data-stu-id="dc99b-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc99b-131">-DefaultProfile</span></span>
<span data-ttu-id="dc99b-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc99b-133">-이름</span><span class="sxs-lookup"><span data-stu-id="dc99b-133">-Name</span></span>
<span data-ttu-id="dc99b-134">Databox Job 이름</span><span class="sxs-lookup"><span data-stu-id="dc99b-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc99b-135">-ResourceGroupName</span></span>
<span data-ttu-id="dc99b-136">Databox Job 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dc99b-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc99b-137">-ResourceId</span></span>
<span data-ttu-id="dc99b-138">Databox Job 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="dc99b-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc99b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc99b-139">CommonParameters</span></span>
<span data-ttu-id="dc99b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc99b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc99b-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc99b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc99b-142">입력</span><span class="sxs-lookup"><span data-stu-id="dc99b-142">INPUTS</span></span>

### <span data-ttu-id="dc99b-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc99b-143">System.String</span></span>

## <span data-ttu-id="dc99b-144">출력</span><span class="sxs-lookup"><span data-stu-id="dc99b-144">OUTPUTS</span></span>

### <span data-ttu-id="dc99b-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="dc99b-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="dc99b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="dc99b-146">NOTES</span></span>

## <span data-ttu-id="dc99b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc99b-147">RELATED LINKS</span></span>
