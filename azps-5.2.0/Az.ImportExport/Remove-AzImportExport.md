---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364498"
---
# <span data-ttu-id="4dc56-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4dc56-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="4dc56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc56-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc56-103">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-103">Deletes an existing job.</span></span>
<span data-ttu-id="4dc56-104">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="4dc56-105">구문</span><span class="sxs-lookup"><span data-stu-id="4dc56-105">SYNTAX</span></span>

### <span data-ttu-id="4dc56-106">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4dc56-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4dc56-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4dc56-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4dc56-108">설명</span><span class="sxs-lookup"><span data-stu-id="4dc56-108">DESCRIPTION</span></span>
<span data-ttu-id="4dc56-109">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-109">Deletes an existing job.</span></span>
<span data-ttu-id="4dc56-110">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="4dc56-111">예제</span><span class="sxs-lookup"><span data-stu-id="4dc56-111">EXAMPLES</span></span>

### <span data-ttu-id="4dc56-112">예제 1: resourceGroup 및 서버 이름으로 ImportExport 작업 제거</span><span class="sxs-lookup"><span data-stu-id="4dc56-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="4dc56-113">이 cmdlet은 resourceGroup 및 서버 이름으로 ImportExport 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="4dc56-114">예제 2: ID로 ImportExport 작업 제거</span><span class="sxs-lookup"><span data-stu-id="4dc56-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="4dc56-115">이러한 cmdlet은 ID에 의해 ImportExport 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="4dc56-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc56-116">PARAMETERS</span></span>

### <span data-ttu-id="4dc56-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4dc56-117">-AcceptLanguage</span></span>
<span data-ttu-id="4dc56-118">응답에 대한 기본 설정 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4dc56-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc56-119">-DefaultProfile</span></span>
<span data-ttu-id="4dc56-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc56-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dc56-121">-InputObject</span></span>
<span data-ttu-id="4dc56-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4dc56-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4dc56-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4dc56-123">-Name</span></span>
<span data-ttu-id="4dc56-124">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="4dc56-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dc56-125">-PassThru</span></span>
<span data-ttu-id="4dc56-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4dc56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc56-127">-ResourceGroupName</span></span>
<span data-ttu-id="4dc56-128">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="4dc56-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dc56-129">-SubscriptionId</span></span>
<span data-ttu-id="4dc56-130">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="4dc56-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dc56-131">-Confirm</span></span>
<span data-ttu-id="4dc56-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc56-133">-WhatIf</span></span>
<span data-ttu-id="4dc56-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4dc56-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc56-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc56-136">CommonParameters</span></span>
<span data-ttu-id="4dc56-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc56-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4dc56-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc56-139">입력</span><span class="sxs-lookup"><span data-stu-id="4dc56-139">INPUTS</span></span>

### <span data-ttu-id="4dc56-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="4dc56-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="4dc56-141">출력</span><span class="sxs-lookup"><span data-stu-id="4dc56-141">OUTPUTS</span></span>

### <span data-ttu-id="4dc56-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dc56-142">System.Boolean</span></span>

## <span data-ttu-id="4dc56-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dc56-143">NOTES</span></span>

<span data-ttu-id="4dc56-144">별칭</span><span class="sxs-lookup"><span data-stu-id="4dc56-144">ALIASES</span></span>

<span data-ttu-id="4dc56-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4dc56-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4dc56-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dc56-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4dc56-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4dc56-148">INPUTOBJECT: <IImportExportIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dc56-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dc56-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4dc56-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dc56-150">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="4dc56-151">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="4dc56-152">예를 들어 미국 서부 또는 westus입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="4dc56-153">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="4dc56-154">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc56-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="4dc56-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dc56-155">RELATED LINKS</span></span>

