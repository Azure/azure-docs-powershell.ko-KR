---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496125"
---
# <span data-ttu-id="43bc1-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="43bc1-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="43bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="43bc1-103">기존 CommunicationService를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="43bc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="43bc1-104">SYNTAX</span></span>

### <span data-ttu-id="43bc1-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="43bc1-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43bc1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43bc1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43bc1-107">설명</span><span class="sxs-lookup"><span data-stu-id="43bc1-107">DESCRIPTION</span></span>
<span data-ttu-id="43bc1-108">기존 CommunicationService를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="43bc1-109">예제</span><span class="sxs-lookup"><span data-stu-id="43bc1-109">EXAMPLES</span></span>

### <span data-ttu-id="43bc1-110">예제 1: 태그가 있는 기존 ACS 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="43bc1-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="43bc1-111">지정된 ACS 리소스에 지정된 태그를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="43bc1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43bc1-112">PARAMETERS</span></span>

### <span data-ttu-id="43bc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bc1-113">-DefaultProfile</span></span>
<span data-ttu-id="43bc1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43bc1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43bc1-115">-InputObject</span></span>
<span data-ttu-id="43bc1-116">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="43bc1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43bc1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43bc1-117">-Name</span></span>
<span data-ttu-id="43bc1-118">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bc1-119">-ResourceGroupName</span></span>
<span data-ttu-id="43bc1-120">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="43bc1-121">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43bc1-122">-SubscriptionId</span></span>
<span data-ttu-id="43bc1-123">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="43bc1-124">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="43bc1-125">-Tag</span></span>
<span data-ttu-id="43bc1-126">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43bc1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43bc1-127">-Confirm</span></span>
<span data-ttu-id="43bc1-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43bc1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43bc1-129">-WhatIf</span></span>
<span data-ttu-id="43bc1-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43bc1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43bc1-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43bc1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bc1-132">CommonParameters</span></span>
<span data-ttu-id="43bc1-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bc1-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43bc1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bc1-135">입력</span><span class="sxs-lookup"><span data-stu-id="43bc1-135">INPUTS</span></span>

### <span data-ttu-id="43bc1-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="43bc1-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="43bc1-137">출력</span><span class="sxs-lookup"><span data-stu-id="43bc1-137">OUTPUTS</span></span>

### <span data-ttu-id="43bc1-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="43bc1-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="43bc1-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43bc1-139">NOTES</span></span>

<span data-ttu-id="43bc1-140">별칭</span><span class="sxs-lookup"><span data-stu-id="43bc1-140">ALIASES</span></span>

<span data-ttu-id="43bc1-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="43bc1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43bc1-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43bc1-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43bc1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43bc1-144">INPUTOBJECT: <ICommunicationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="43bc1-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43bc1-145">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="43bc1-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="43bc1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43bc1-147">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="43bc1-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="43bc1-148">`[OperationId <String>]`: 진행 중 비동기 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="43bc1-149">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="43bc1-150">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="43bc1-151">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="43bc1-152">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="43bc1-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43bc1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43bc1-153">RELATED LINKS</span></span>

