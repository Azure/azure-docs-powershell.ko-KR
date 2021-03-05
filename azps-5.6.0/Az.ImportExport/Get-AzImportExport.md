---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 8825cb9b3d4a2efcd6a326244139950e431d71f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964635"
---
# <span data-ttu-id="14c1c-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="14c1c-101">Get-AzImportExport</span></span>

## <span data-ttu-id="14c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="14c1c-103">기존 작업의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="14c1c-104">구문</span><span class="sxs-lookup"><span data-stu-id="14c1c-104">SYNTAX</span></span>

### <span data-ttu-id="14c1c-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="14c1c-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14c1c-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="14c1c-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14c1c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14c1c-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14c1c-108">List1</span><span class="sxs-lookup"><span data-stu-id="14c1c-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="14c1c-109">설명</span><span class="sxs-lookup"><span data-stu-id="14c1c-109">DESCRIPTION</span></span>
<span data-ttu-id="14c1c-110">기존 작업의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="14c1c-111">예제</span><span class="sxs-lookup"><span data-stu-id="14c1c-111">EXAMPLES</span></span>

### <span data-ttu-id="14c1c-112">예제 1: 기본 컨텍스트로 ImportExport 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="14c1c-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14c1c-113">이 cmdlet은 기본 컨텍스트를 통해 ImportExport 작업을 가져온다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="14c1c-114">예제 2: 리소스 그룹 및 작업 이름에 따라 ImportExport 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="14c1c-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14c1c-115">이 cmdlet은 리소스 그룹 및 작업 이름에 따라 ImportExport 작업을 가져온다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="14c1c-116">예제 3: 지정된 리소스 그룹에 있는 모든 ImportExport 작업 나열</span><span class="sxs-lookup"><span data-stu-id="14c1c-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14c1c-117">이 cmdlet은 지정된 리소스 그룹에 있는 모든 ImportExport 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="14c1c-118">예제 4: ID로 ImportExport 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="14c1c-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14c1c-119">이 cmdlet 목록은 ID로 ImportExport 작업을 가져온다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="14c1c-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14c1c-120">PARAMETERS</span></span>

### <span data-ttu-id="14c1c-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="14c1c-121">-AcceptLanguage</span></span>
<span data-ttu-id="14c1c-122">응답에 대한 기본 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="14c1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c1c-123">-DefaultProfile</span></span>
<span data-ttu-id="14c1c-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="14c1c-125">-Filter</span></span>
<span data-ttu-id="14c1c-126">결과를 특정 조건으로 제한하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14c1c-127">-InputObject</span></span>
<span data-ttu-id="14c1c-128">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="14c1c-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="14c1c-129">-Name</span></span>
<span data-ttu-id="14c1c-130">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c1c-131">-ResourceGroupName</span></span>
<span data-ttu-id="14c1c-132">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14c1c-133">-SubscriptionId</span></span>
<span data-ttu-id="14c1c-134">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-135">-Top</span><span class="sxs-lookup"><span data-stu-id="14c1c-135">-Top</span></span>
<span data-ttu-id="14c1c-136">반환해야 하는 작업 수를 지정하는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="14c1c-137">값은 100을 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c1c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c1c-138">CommonParameters</span></span>
<span data-ttu-id="14c1c-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c1c-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14c1c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c1c-141">입력</span><span class="sxs-lookup"><span data-stu-id="14c1c-141">INPUTS</span></span>

### <span data-ttu-id="14c1c-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="14c1c-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="14c1c-143">출력</span><span class="sxs-lookup"><span data-stu-id="14c1c-143">OUTPUTS</span></span>

### <span data-ttu-id="14c1c-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="14c1c-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="14c1c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14c1c-145">NOTES</span></span>

<span data-ttu-id="14c1c-146">별칭</span><span class="sxs-lookup"><span data-stu-id="14c1c-146">ALIASES</span></span>

<span data-ttu-id="14c1c-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="14c1c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14c1c-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14c1c-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14c1c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14c1c-150">INPUTOBJECT <IImportExportIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="14c1c-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14c1c-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="14c1c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14c1c-152">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="14c1c-153">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="14c1c-154">예를 들어 미국 서부 또는 서부.</span><span class="sxs-lookup"><span data-stu-id="14c1c-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="14c1c-155">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="14c1c-156">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14c1c-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="14c1c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14c1c-157">RELATED LINKS</span></span>

