---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: c4ba805ca2f8f89fcc3ed23747f71c9efff01d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977104"
---
# <span data-ttu-id="3eb5e-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3eb5e-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="3eb5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb5e-103">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-103">Deletes an existing job.</span></span>
<span data-ttu-id="3eb5e-104">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="3eb5e-105">구문</span><span class="sxs-lookup"><span data-stu-id="3eb5e-105">SYNTAX</span></span>

### <span data-ttu-id="3eb5e-106">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="3eb5e-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3eb5e-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3eb5e-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3eb5e-108">설명</span><span class="sxs-lookup"><span data-stu-id="3eb5e-108">DESCRIPTION</span></span>
<span data-ttu-id="3eb5e-109">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-109">Deletes an existing job.</span></span>
<span data-ttu-id="3eb5e-110">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="3eb5e-111">예제</span><span class="sxs-lookup"><span data-stu-id="3eb5e-111">EXAMPLES</span></span>

### <span data-ttu-id="3eb5e-112">예제 1: ResourceGroup 및 서버 이름으로 ImportExport 작업 제거</span><span class="sxs-lookup"><span data-stu-id="3eb5e-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="3eb5e-113">이 cmdlet은 ResourceGroup 및 서버 이름으로 ImportExport 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="3eb5e-114">예제 2: ID로 ImportExport 작업 제거</span><span class="sxs-lookup"><span data-stu-id="3eb5e-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="3eb5e-115">이러한 cmdlet은 ID로 ImportExport 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="3eb5e-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3eb5e-116">PARAMETERS</span></span>

### <span data-ttu-id="3eb5e-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3eb5e-117">-AcceptLanguage</span></span>
<span data-ttu-id="3eb5e-118">응답에 대한 기본 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3eb5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb5e-119">-DefaultProfile</span></span>
<span data-ttu-id="3eb5e-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb5e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb5e-121">-InputObject</span></span>
<span data-ttu-id="3eb5e-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3eb5e-123">-Name</span></span>
<span data-ttu-id="3eb5e-124">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eb5e-125">-PassThru</span></span>
<span data-ttu-id="3eb5e-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-126">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3eb5e-128">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3eb5e-129">-SubscriptionId</span></span>
<span data-ttu-id="3eb5e-130">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-130">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-131">-확인</span><span class="sxs-lookup"><span data-stu-id="3eb5e-131">-Confirm</span></span>
<span data-ttu-id="3eb5e-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb5e-133">-WhatIf</span></span>
<span data-ttu-id="3eb5e-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb5e-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb5e-136">CommonParameters</span></span>
<span data-ttu-id="3eb5e-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb5e-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eb5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb5e-139">입력</span><span class="sxs-lookup"><span data-stu-id="3eb5e-139">INPUTS</span></span>

### <span data-ttu-id="3eb5e-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="3eb5e-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3eb5e-141">출력</span><span class="sxs-lookup"><span data-stu-id="3eb5e-141">OUTPUTS</span></span>

### <span data-ttu-id="3eb5e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3eb5e-142">System.Boolean</span></span>

## <span data-ttu-id="3eb5e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3eb5e-143">NOTES</span></span>

<span data-ttu-id="3eb5e-144">별칭</span><span class="sxs-lookup"><span data-stu-id="3eb5e-144">ALIASES</span></span>

<span data-ttu-id="3eb5e-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3eb5e-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3eb5e-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3eb5e-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3eb5e-148">INPUTOBJECT <IImportExportIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3eb5e-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3eb5e-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3eb5e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3eb5e-150">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3eb5e-151">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3eb5e-152">예를 들어 미국 서부 또는 서부.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="3eb5e-153">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3eb5e-154">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb5e-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3eb5e-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3eb5e-155">RELATED LINKS</span></span>

