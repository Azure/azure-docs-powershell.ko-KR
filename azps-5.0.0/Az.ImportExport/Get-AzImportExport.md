---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217802"
---
# <span data-ttu-id="70793-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="70793-101">Get-AzImportExport</span></span>

## <span data-ttu-id="70793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70793-102">SYNOPSIS</span></span>
<span data-ttu-id="70793-103">기존 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70793-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="70793-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70793-104">SYNTAX</span></span>

### <span data-ttu-id="70793-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="70793-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70793-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="70793-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70793-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70793-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70793-108">List1</span><span class="sxs-lookup"><span data-stu-id="70793-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="70793-109">설명은</span><span class="sxs-lookup"><span data-stu-id="70793-109">DESCRIPTION</span></span>
<span data-ttu-id="70793-110">기존 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70793-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="70793-111">예제의</span><span class="sxs-lookup"><span data-stu-id="70793-111">EXAMPLES</span></span>

### <span data-ttu-id="70793-112">예제 1: 기본 컨텍스트를 사용 하 여 ImportExport 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="70793-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="70793-113">이 cmdlet은 기본 컨텍스트를 사용 하 여 가져오기 내보내기 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70793-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="70793-114">예제 2: 리소스 그룹 및 작업 이름을 기준으로 가져오기 내보내기 작업</span><span class="sxs-lookup"><span data-stu-id="70793-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="70793-115">이 cmdlet은 리소스 그룹과 작업 이름에 따라 가져오기 내보내기 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70793-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="70793-116">예제 3: 지정 된 리소스 그룹의 모든 ImportExport 작업 나열</span><span class="sxs-lookup"><span data-stu-id="70793-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="70793-117">이 cmdlet은 지정 된 리소스 그룹의 모든 ImportExport 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="70793-118">예제 4: id 별 ImportExport 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="70793-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="70793-119">이 cmdlet 목록은 id를 기준으로 가져오기 내보내기 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70793-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="70793-120">변수</span><span class="sxs-lookup"><span data-stu-id="70793-120">PARAMETERS</span></span>

### <span data-ttu-id="70793-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="70793-121">-AcceptLanguage</span></span>
<span data-ttu-id="70793-122">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="70793-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70793-123">-DefaultProfile</span></span>
<span data-ttu-id="70793-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70793-125">-필터</span><span class="sxs-lookup"><span data-stu-id="70793-125">-Filter</span></span>
<span data-ttu-id="70793-126">특정 조건으로 결과를 제한 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70793-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="70793-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70793-127">-InputObject</span></span>
<span data-ttu-id="70793-128">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70793-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="70793-129">-이름</span><span class="sxs-lookup"><span data-stu-id="70793-129">-Name</span></span>
<span data-ttu-id="70793-130">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="70793-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70793-131">-ResourceGroupName</span></span>
<span data-ttu-id="70793-132">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="70793-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70793-133">-SubscriptionId</span></span>
<span data-ttu-id="70793-134">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="70793-135">-위쪽</span><span class="sxs-lookup"><span data-stu-id="70793-135">-Top</span></span>
<span data-ttu-id="70793-136">반환할 최대 작업 수를 지정 하는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="70793-137">값은 100을 초과할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70793-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="70793-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70793-138">CommonParameters</span></span>
<span data-ttu-id="70793-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70793-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70793-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70793-141">입력</span><span class="sxs-lookup"><span data-stu-id="70793-141">INPUTS</span></span>

### <span data-ttu-id="70793-142">IImportExportIdentity 내보내기. i m a.</span><span class="sxs-lookup"><span data-stu-id="70793-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="70793-143">출력</span><span class="sxs-lookup"><span data-stu-id="70793-143">OUTPUTS</span></span>

### <span data-ttu-id="70793-144">Api20161101 내보내기. i i a PowerShell. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="70793-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="70793-145">상속자</span><span class="sxs-lookup"><span data-stu-id="70793-145">NOTES</span></span>

<span data-ttu-id="70793-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="70793-146">ALIASES</span></span>

<span data-ttu-id="70793-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="70793-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70793-148">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70793-149">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="70793-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70793-150">INPUTOBJECT <IImportExportIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="70793-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70793-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="70793-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70793-152">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="70793-153">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="70793-154">예를 들어 미국/동 또는 westus.</span><span class="sxs-lookup"><span data-stu-id="70793-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="70793-155">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내에서 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="70793-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="70793-156">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70793-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="70793-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70793-157">RELATED LINKS</span></span>

