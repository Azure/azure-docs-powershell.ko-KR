---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 53127b970c3c2f588a54eaec3dcd9ea1174a7053
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991573"
---
# <span data-ttu-id="7fc3c-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="7fc3c-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="7fc3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc3c-103">기존 CommunicationService를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="7fc3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fc3c-104">SYNTAX</span></span>

### <span data-ttu-id="7fc3c-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="7fc3c-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fc3c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7fc3c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fc3c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7fc3c-107">DESCRIPTION</span></span>
<span data-ttu-id="7fc3c-108">기존 CommunicationService를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="7fc3c-109">예제</span><span class="sxs-lookup"><span data-stu-id="7fc3c-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc3c-110">예제 1: 태그가 있는 기존 ACS 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="7fc3c-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="7fc3c-111">지정된 ACS 리소스에 지정된 태그를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="7fc3c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7fc3c-112">PARAMETERS</span></span>

### <span data-ttu-id="7fc3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc3c-113">-DefaultProfile</span></span>
<span data-ttu-id="7fc3c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc3c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc3c-115">-InputObject</span></span>
<span data-ttu-id="7fc3c-116">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fc3c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7fc3c-117">-Name</span></span>
<span data-ttu-id="7fc3c-118">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-118">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="7fc3c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc3c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fc3c-120">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7fc3c-121">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7fc3c-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fc3c-122">-SubscriptionId</span></span>
<span data-ttu-id="7fc3c-123">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fc3c-124">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7fc3c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7fc3c-125">-Tag</span></span>
<span data-ttu-id="7fc3c-126">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="7fc3c-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7fc3c-127">-Confirm</span></span>
<span data-ttu-id="7fc3c-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc3c-129">-WhatIf</span></span>
<span data-ttu-id="7fc3c-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc3c-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc3c-132">CommonParameters</span></span>
<span data-ttu-id="7fc3c-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc3c-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fc3c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc3c-135">입력</span><span class="sxs-lookup"><span data-stu-id="7fc3c-135">INPUTS</span></span>

### <span data-ttu-id="7fc3c-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="7fc3c-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="7fc3c-137">출력</span><span class="sxs-lookup"><span data-stu-id="7fc3c-137">OUTPUTS</span></span>

### <span data-ttu-id="7fc3c-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="7fc3c-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="7fc3c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fc3c-139">NOTES</span></span>

<span data-ttu-id="7fc3c-140">별칭</span><span class="sxs-lookup"><span data-stu-id="7fc3c-140">ALIASES</span></span>

<span data-ttu-id="7fc3c-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7fc3c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fc3c-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fc3c-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fc3c-144">INPUTOBJECT <ICommunicationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7fc3c-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fc3c-145">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="7fc3c-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7fc3c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fc3c-147">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="7fc3c-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="7fc3c-148">`[OperationId <String>]`: 진행하는 비동기 작업의 ID</span><span class="sxs-lookup"><span data-stu-id="7fc3c-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="7fc3c-149">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7fc3c-150">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7fc3c-151">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="7fc3c-152">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc3c-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7fc3c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fc3c-153">RELATED LINKS</span></span>

