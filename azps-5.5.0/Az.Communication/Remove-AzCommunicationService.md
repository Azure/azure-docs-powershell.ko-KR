---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177793"
---
# <span data-ttu-id="e620b-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="e620b-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="e620b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e620b-102">SYNOPSIS</span></span>
<span data-ttu-id="e620b-103">CommunicationService를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="e620b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e620b-104">SYNTAX</span></span>

### <span data-ttu-id="e620b-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="e620b-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e620b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e620b-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e620b-107">설명</span><span class="sxs-lookup"><span data-stu-id="e620b-107">DESCRIPTION</span></span>
<span data-ttu-id="e620b-108">CommunicationService를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="e620b-109">예제</span><span class="sxs-lookup"><span data-stu-id="e620b-109">EXAMPLES</span></span>

### <span data-ttu-id="e620b-110">예제 1: 지정된 Azure Communication 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="e620b-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="e620b-111">Azure Communication 리소스를 제거/삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="e620b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e620b-112">PARAMETERS</span></span>

### <span data-ttu-id="e620b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e620b-113">-AsJob</span></span>
<span data-ttu-id="e620b-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="e620b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e620b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e620b-115">-DefaultProfile</span></span>
<span data-ttu-id="e620b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e620b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e620b-117">-InputObject</span></span>
<span data-ttu-id="e620b-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e620b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e620b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e620b-119">-Name</span></span>
<span data-ttu-id="e620b-120">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e620b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e620b-121">-NoWait</span></span>
<span data-ttu-id="e620b-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="e620b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e620b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e620b-123">-PassThru</span></span>
<span data-ttu-id="e620b-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e620b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e620b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e620b-126">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e620b-127">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e620b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e620b-128">-SubscriptionId</span></span>
<span data-ttu-id="e620b-129">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e620b-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e620b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e620b-131">-Confirm</span></span>
<span data-ttu-id="e620b-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e620b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e620b-133">-WhatIf</span></span>
<span data-ttu-id="e620b-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e620b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e620b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e620b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e620b-136">CommonParameters</span></span>
<span data-ttu-id="e620b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e620b-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e620b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e620b-139">입력</span><span class="sxs-lookup"><span data-stu-id="e620b-139">INPUTS</span></span>

### <span data-ttu-id="e620b-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="e620b-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="e620b-141">출력</span><span class="sxs-lookup"><span data-stu-id="e620b-141">OUTPUTS</span></span>

### <span data-ttu-id="e620b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e620b-142">System.Boolean</span></span>

## <span data-ttu-id="e620b-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e620b-143">NOTES</span></span>

<span data-ttu-id="e620b-144">별칭</span><span class="sxs-lookup"><span data-stu-id="e620b-144">ALIASES</span></span>

<span data-ttu-id="e620b-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e620b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e620b-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e620b-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e620b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e620b-148">INPUTOBJECT: <ICommunicationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e620b-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e620b-149">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="e620b-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e620b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e620b-151">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="e620b-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="e620b-152">`[OperationId <String>]`: 진행 중 비동기 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="e620b-153">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e620b-154">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e620b-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e620b-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e620b-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e620b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e620b-157">RELATED LINKS</span></span>

