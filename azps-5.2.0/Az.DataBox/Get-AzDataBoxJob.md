---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327116"
---
# <span data-ttu-id="c9a2e-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c9a2e-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="c9a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a2e-103">Databox 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="c9a2e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9a2e-104">SYNTAX</span></span>

### <span data-ttu-id="c9a2e-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9a2e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9a2e-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a2e-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9a2e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9a2e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9a2e-108">설명</span><span class="sxs-lookup"><span data-stu-id="c9a2e-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a2e-109">**Get-AzDataBoxJobs** cmdlet은 Azure 구독의 데이터 상자 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="c9a2e-110">리소스 그룹을 지정하면 이 cmdlet은 해당 리소스 그룹 아래에 있는 모든 데이터 상자 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="c9a2e-111">리소스 그룹 이름과 함께 작업 이름을 지정하면 이 cmdlet은 해당 특정 데이터 상자 작업 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="c9a2e-112">구독 ID를 지정하지 않으면 이 cmdlet은 해당 구독의 모든 데이터 상자 작업 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="c9a2e-113">예제</span><span class="sxs-lookup"><span data-stu-id="c9a2e-113">EXAMPLES</span></span>

### <span data-ttu-id="c9a2e-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9a2e-114">Example 1</span></span>
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

<span data-ttu-id="c9a2e-115">Get-AzDataBoxJob 없는 경우 구독에서 모든 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="c9a2e-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="c9a2e-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="c9a2e-117">Get-AzDataBoxJob ResourceGroupName 매개 변수를 사용하여 지정된 리소스 그룹에서 모든 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="c9a2e-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="c9a2e-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c9a2e-119">Get-AzDataBoxJob ResourceGroupName 및 Name을 사용하여 해당 특정 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="c9a2e-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="c9a2e-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c9a2e-121">Get-AzDataBoxJob 지정한 경우 해당 특정 데이터 상자 작업을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="c9a2e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9a2e-122">PARAMETERS</span></span>

### <span data-ttu-id="c9a2e-123">-Aborted</span><span class="sxs-lookup"><span data-stu-id="c9a2e-123">-Aborted</span></span>
<span data-ttu-id="c9a2e-124">매개 변수를 전환하여 중단된 작업 페치</span><span class="sxs-lookup"><span data-stu-id="c9a2e-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="c9a2e-125">-Cancelled</span><span class="sxs-lookup"><span data-stu-id="c9a2e-125">-Cancelled</span></span>
<span data-ttu-id="c9a2e-126">매개 변수를 전환하여 취소된 작업 페치</span><span class="sxs-lookup"><span data-stu-id="c9a2e-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="c9a2e-127">-Completed</span><span class="sxs-lookup"><span data-stu-id="c9a2e-127">-Completed</span></span>
<span data-ttu-id="c9a2e-128">매개 변수를 전환하여 완료된 작업 페치</span><span class="sxs-lookup"><span data-stu-id="c9a2e-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="c9a2e-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="c9a2e-129">-CompletedWithError</span></span>
<span data-ttu-id="c9a2e-130">매개 변수를 전환하여 오류와 함께 완료된 작업을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="c9a2e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a2e-131">-DefaultProfile</span></span>
<span data-ttu-id="c9a2e-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a2e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c9a2e-133">-Name</span></span>
<span data-ttu-id="c9a2e-134">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="c9a2e-134">Databox Job Name</span></span>

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

### <span data-ttu-id="c9a2e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a2e-135">-ResourceGroupName</span></span>
<span data-ttu-id="c9a2e-136">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c9a2e-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="c9a2e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9a2e-137">-ResourceId</span></span>
<span data-ttu-id="c9a2e-138">Databox 작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c9a2e-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="c9a2e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a2e-139">CommonParameters</span></span>
<span data-ttu-id="c9a2e-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a2e-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9a2e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a2e-142">입력</span><span class="sxs-lookup"><span data-stu-id="c9a2e-142">INPUTS</span></span>

### <span data-ttu-id="c9a2e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c9a2e-143">System.String</span></span>

## <span data-ttu-id="c9a2e-144">출력</span><span class="sxs-lookup"><span data-stu-id="c9a2e-144">OUTPUTS</span></span>

### <span data-ttu-id="c9a2e-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c9a2e-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="c9a2e-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9a2e-146">NOTES</span></span>

## <span data-ttu-id="c9a2e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a2e-147">RELATED LINKS</span></span>
