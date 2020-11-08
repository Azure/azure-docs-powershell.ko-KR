---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212215"
---
# <span data-ttu-id="acb2b-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="acb2b-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="acb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="acb2b-103">기존 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-103">Deletes an existing job.</span></span>
<span data-ttu-id="acb2b-104">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="acb2b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="acb2b-105">SYNTAX</span></span>

### <span data-ttu-id="acb2b-106">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="acb2b-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="acb2b-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="acb2b-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acb2b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="acb2b-108">DESCRIPTION</span></span>
<span data-ttu-id="acb2b-109">기존 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-109">Deletes an existing job.</span></span>
<span data-ttu-id="acb2b-110">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="acb2b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="acb2b-111">EXAMPLES</span></span>

### <span data-ttu-id="acb2b-112">예제 1: 리소스 및 서버 이름으로 가져오기 내보내기 작업 제거</span><span class="sxs-lookup"><span data-stu-id="acb2b-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="acb2b-113">이 cmdlet은 resourceGroup 및 서버 이름에 따라 ImportExport 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="acb2b-114">예제 2: id 별 ImportExport 작업 제거</span><span class="sxs-lookup"><span data-stu-id="acb2b-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="acb2b-115">이러한 cmdlet은 id를 기준으로 가져오기 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="acb2b-116">변수</span><span class="sxs-lookup"><span data-stu-id="acb2b-116">PARAMETERS</span></span>

### <span data-ttu-id="acb2b-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="acb2b-117">-AcceptLanguage</span></span>
<span data-ttu-id="acb2b-118">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="acb2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb2b-119">-DefaultProfile</span></span>
<span data-ttu-id="acb2b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acb2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acb2b-121">-InputObject</span></span>
<span data-ttu-id="acb2b-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="acb2b-123">-이름</span><span class="sxs-lookup"><span data-stu-id="acb2b-123">-Name</span></span>
<span data-ttu-id="acb2b-124">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="acb2b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acb2b-125">-PassThru</span></span>
<span data-ttu-id="acb2b-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="acb2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="acb2b-128">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="acb2b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acb2b-129">-SubscriptionId</span></span>
<span data-ttu-id="acb2b-130">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="acb2b-131">-확인</span><span class="sxs-lookup"><span data-stu-id="acb2b-131">-Confirm</span></span>
<span data-ttu-id="acb2b-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acb2b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb2b-133">-WhatIf</span></span>
<span data-ttu-id="acb2b-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acb2b-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acb2b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb2b-136">CommonParameters</span></span>
<span data-ttu-id="acb2b-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb2b-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="acb2b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb2b-139">입력</span><span class="sxs-lookup"><span data-stu-id="acb2b-139">INPUTS</span></span>

### <span data-ttu-id="acb2b-140">IImportExportIdentity 내보내기. i m a.</span><span class="sxs-lookup"><span data-stu-id="acb2b-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="acb2b-141">출력</span><span class="sxs-lookup"><span data-stu-id="acb2b-141">OUTPUTS</span></span>

### <span data-ttu-id="acb2b-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="acb2b-142">System.Boolean</span></span>

## <span data-ttu-id="acb2b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="acb2b-143">NOTES</span></span>

<span data-ttu-id="acb2b-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="acb2b-144">ALIASES</span></span>

<span data-ttu-id="acb2b-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="acb2b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acb2b-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acb2b-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="acb2b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acb2b-148">INPUTOBJECT <IImportExportIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="acb2b-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="acb2b-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="acb2b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="acb2b-150">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="acb2b-151">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="acb2b-152">예를 들어 미국/동 또는 westus.</span><span class="sxs-lookup"><span data-stu-id="acb2b-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="acb2b-153">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내에서 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="acb2b-154">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="acb2b-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="acb2b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acb2b-155">RELATED LINKS</span></span>

