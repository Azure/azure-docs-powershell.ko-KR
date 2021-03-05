---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: 4b9186265287c52c27cff6cb1a7f0d0570949e76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991615"
---
# <span data-ttu-id="65391-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="65391-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="65391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65391-102">SYNOPSIS</span></span>
<span data-ttu-id="65391-103">CommunicationService 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="65391-104">PrimaryKey 및 SecondaryKey는 동시에 다시 생성될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="65391-105">구문</span><span class="sxs-lookup"><span data-stu-id="65391-105">SYNTAX</span></span>

### <span data-ttu-id="65391-106">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="65391-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="65391-107">다시 생성</span><span class="sxs-lookup"><span data-stu-id="65391-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65391-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65391-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65391-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="65391-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65391-110">설명</span><span class="sxs-lookup"><span data-stu-id="65391-110">DESCRIPTION</span></span>
<span data-ttu-id="65391-111">CommunicationService 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="65391-112">PrimaryKey 및 SecondaryKey는 동시에 다시 생성될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="65391-113">예제</span><span class="sxs-lookup"><span data-stu-id="65391-113">EXAMPLES</span></span>

### <span data-ttu-id="65391-114">예제 1: IRegenerateKeyParameters 해시테이블을 사용하여 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="65391-115">이전 기본 키를 무효화하고 새 키를 다시 생성하고 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="65391-116">예제 2: KeyType을 사용하여 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="65391-117">이전 보조 키를 무효화하고 새 키를 다시 생성하고 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="65391-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65391-118">PARAMETERS</span></span>

### <span data-ttu-id="65391-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="65391-119">-CommunicationServiceName</span></span>
<span data-ttu-id="65391-120">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65391-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65391-121">-DefaultProfile</span></span>
<span data-ttu-id="65391-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65391-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65391-123">-InputObject</span></span>
<span data-ttu-id="65391-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="65391-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65391-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="65391-125">-KeyType</span></span>
<span data-ttu-id="65391-126">다시 생성하는 keyType입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-126">The keyType to regenerate.</span></span>
<span data-ttu-id="65391-127">'기본' 또는 '보조'(대소문자 무감소식)되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65391-128">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="65391-128">-Parameter</span></span>
<span data-ttu-id="65391-129">매개 변수는 액세스 키를 다시 생성하는 요청을 설명합니다. 구성하기 위해 매개 변수 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="65391-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65391-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65391-130">-ResourceGroupName</span></span>
<span data-ttu-id="65391-131">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="65391-132">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65391-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65391-133">-SubscriptionId</span></span>
<span data-ttu-id="65391-134">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="65391-135">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65391-136">-확인</span><span class="sxs-lookup"><span data-stu-id="65391-136">-Confirm</span></span>
<span data-ttu-id="65391-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65391-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65391-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65391-138">-WhatIf</span></span>
<span data-ttu-id="65391-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65391-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65391-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65391-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65391-141">CommonParameters</span></span>
<span data-ttu-id="65391-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65391-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65391-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65391-144">입력</span><span class="sxs-lookup"><span data-stu-id="65391-144">INPUTS</span></span>

### <span data-ttu-id="65391-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="65391-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="65391-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="65391-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="65391-147">출력</span><span class="sxs-lookup"><span data-stu-id="65391-147">OUTPUTS</span></span>

### <span data-ttu-id="65391-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="65391-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="65391-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65391-149">NOTES</span></span>

<span data-ttu-id="65391-150">별칭</span><span class="sxs-lookup"><span data-stu-id="65391-150">ALIASES</span></span>

<span data-ttu-id="65391-151">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="65391-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65391-152">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65391-153">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65391-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65391-154">INPUTOBJECT <ICommunicationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="65391-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65391-155">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="65391-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="65391-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65391-157">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="65391-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="65391-158">`[OperationId <String>]`: 진행하는 비동기 작업의 ID</span><span class="sxs-lookup"><span data-stu-id="65391-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="65391-159">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="65391-160">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="65391-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65391-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="65391-162">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="65391-163">매개 변수 : 매개 변수는 액세스 키를 <IRegenerateKeyParameters> 다시 생성하는 요청을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="65391-164">`[KeyType <KeyType?>]`: 다시 생성하는 keyType입니다.</span><span class="sxs-lookup"><span data-stu-id="65391-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="65391-165">'기본' 또는 '보조'(대소문자 무감소식)되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65391-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="65391-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65391-166">RELATED LINKS</span></span>

