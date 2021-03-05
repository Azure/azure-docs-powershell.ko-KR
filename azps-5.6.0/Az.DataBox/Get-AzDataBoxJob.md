---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: af406af487e03c429a21a99799083f67d0fabf53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998116"
---
# <span data-ttu-id="8de24-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8de24-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="8de24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de24-102">SYNOPSIS</span></span>
<span data-ttu-id="8de24-103">Databox Jobs에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="8de24-104">구문</span><span class="sxs-lookup"><span data-stu-id="8de24-104">SYNTAX</span></span>

### <span data-ttu-id="8de24-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8de24-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8de24-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de24-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8de24-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de24-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8de24-108">설명</span><span class="sxs-lookup"><span data-stu-id="8de24-108">DESCRIPTION</span></span>
<span data-ttu-id="8de24-109">**Get-AzDataBoxJobs** cmdlet은 Azure 구독의 데이터 상자 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="8de24-110">리소스 그룹을 지정하는 경우 이 cmdlet은 해당 리소스 그룹 아래에서 모든 데이터 상자 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="8de24-111">리소스 그룹 이름과 함께 작업 이름을 지정하는 경우 이 cmdlet은 해당 특정 데이터 상자 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="8de24-112">구독 ID 외의 아무 것도 지정하지 않으면 이 cmdlet은 해당 구독 아래에서 모든 데이터 상자 작업의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="8de24-113">예제</span><span class="sxs-lookup"><span data-stu-id="8de24-113">EXAMPLES</span></span>

### <span data-ttu-id="8de24-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="8de24-114">Example 1</span></span>
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

<span data-ttu-id="8de24-115">Get-AzDataBoxJob 매개 변수가 없는 경우 구독에서 모든 데이터 상자 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="8de24-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="8de24-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="8de24-117">Get-AzDataBoxJob ResourceGroupName 매개 변수를 사용하여 지정된 리소스 그룹에서 모든 데이터 상자 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="8de24-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="8de24-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="8de24-119">Get-AzDataBoxJob ResourceGroupName 및 Name을 사용하여 해당 특정 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="8de24-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="8de24-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="8de24-121">Get-AzDataBoxJob 지정한 경우 해당 특정 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="8de24-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8de24-122">PARAMETERS</span></span>

### <span data-ttu-id="8de24-123">-중단</span><span class="sxs-lookup"><span data-stu-id="8de24-123">-Aborted</span></span>
<span data-ttu-id="8de24-124">매개 변수를 전환하여 중단된 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="8de24-125">-취소</span><span class="sxs-lookup"><span data-stu-id="8de24-125">-Cancelled</span></span>
<span data-ttu-id="8de24-126">매개 변수를 전환하여 취소된 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="8de24-127">-완료</span><span class="sxs-lookup"><span data-stu-id="8de24-127">-Completed</span></span>
<span data-ttu-id="8de24-128">매개 변수를 전환하여 완료된 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="8de24-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="8de24-129">-CompletedWithError</span></span>
<span data-ttu-id="8de24-130">매개 변수를 전환하여 오류로 완료된 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="8de24-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de24-131">-DefaultProfile</span></span>
<span data-ttu-id="8de24-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de24-133">-Name</span><span class="sxs-lookup"><span data-stu-id="8de24-133">-Name</span></span>
<span data-ttu-id="8de24-134">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="8de24-134">Databox Job Name</span></span>

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

### <span data-ttu-id="8de24-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de24-135">-ResourceGroupName</span></span>
<span data-ttu-id="8de24-136">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8de24-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="8de24-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8de24-137">-ResourceId</span></span>
<span data-ttu-id="8de24-138">Databox 작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8de24-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="8de24-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de24-139">CommonParameters</span></span>
<span data-ttu-id="8de24-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8de24-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de24-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8de24-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de24-142">입력</span><span class="sxs-lookup"><span data-stu-id="8de24-142">INPUTS</span></span>

### <span data-ttu-id="8de24-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8de24-143">System.String</span></span>

## <span data-ttu-id="8de24-144">출력</span><span class="sxs-lookup"><span data-stu-id="8de24-144">OUTPUTS</span></span>

### <span data-ttu-id="8de24-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="8de24-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="8de24-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8de24-146">NOTES</span></span>

## <span data-ttu-id="8de24-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8de24-147">RELATED LINKS</span></span>
