---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177796"
---
# <span data-ttu-id="20630-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="20630-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="20630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20630-102">SYNOPSIS</span></span>
<span data-ttu-id="20630-103">CommunicationService 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="20630-104">PrimaryKey 및 SecondaryKey는 동시에 다시 생성될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="20630-105">구문</span><span class="sxs-lookup"><span data-stu-id="20630-105">SYNTAX</span></span>

### <span data-ttu-id="20630-106">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="20630-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="20630-107">다시 생성</span><span class="sxs-lookup"><span data-stu-id="20630-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20630-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20630-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20630-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="20630-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20630-110">설명</span><span class="sxs-lookup"><span data-stu-id="20630-110">DESCRIPTION</span></span>
<span data-ttu-id="20630-111">CommunicationService 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="20630-112">PrimaryKey 및 SecondaryKey는 동시에 다시 생성될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="20630-113">예제</span><span class="sxs-lookup"><span data-stu-id="20630-113">EXAMPLES</span></span>

### <span data-ttu-id="20630-114">예제 1: IRegenerateKeyParameters 해시테이블을 사용하여 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="20630-115">이전 기본 키를 무효화하고, 새 키를 다시 생성하고, 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="20630-116">예제 2: KeyType을 사용하여 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="20630-117">이전 보조 키를 무효화하고, 새 키를 다시 생성하고, 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="20630-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20630-118">PARAMETERS</span></span>

### <span data-ttu-id="20630-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="20630-119">-CommunicationServiceName</span></span>
<span data-ttu-id="20630-120">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="20630-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20630-121">-DefaultProfile</span></span>
<span data-ttu-id="20630-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20630-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20630-123">-InputObject</span></span>
<span data-ttu-id="20630-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="20630-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20630-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="20630-125">-KeyType</span></span>
<span data-ttu-id="20630-126">다시 생성할 keyType입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-126">The keyType to regenerate.</span></span>
<span data-ttu-id="20630-127">'primary' 또는 'secondary'(대소문자 무관)입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

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

### <span data-ttu-id="20630-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="20630-128">-Parameter</span></span>
<span data-ttu-id="20630-129">매개 변수는 액세스 키를 다시 생성하는 요청을 설명합니다. 구성을 위해 매개 변수 속성에 대한 NOTES 섹션 및 해시 테이블 만들기를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20630-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="20630-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20630-130">-ResourceGroupName</span></span>
<span data-ttu-id="20630-131">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="20630-132">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="20630-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20630-133">-SubscriptionId</span></span>
<span data-ttu-id="20630-134">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="20630-135">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="20630-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20630-136">-Confirm</span></span>
<span data-ttu-id="20630-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20630-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20630-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20630-138">-WhatIf</span></span>
<span data-ttu-id="20630-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="20630-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20630-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20630-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20630-141">CommonParameters</span></span>
<span data-ttu-id="20630-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20630-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20630-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20630-144">입력</span><span class="sxs-lookup"><span data-stu-id="20630-144">INPUTS</span></span>

### <span data-ttu-id="20630-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="20630-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="20630-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="20630-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="20630-147">출력</span><span class="sxs-lookup"><span data-stu-id="20630-147">OUTPUTS</span></span>

### <span data-ttu-id="20630-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="20630-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="20630-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20630-149">NOTES</span></span>

<span data-ttu-id="20630-150">별칭</span><span class="sxs-lookup"><span data-stu-id="20630-150">ALIASES</span></span>

<span data-ttu-id="20630-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="20630-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20630-152">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20630-153">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20630-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20630-154">INPUTOBJECT: <ICommunicationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="20630-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20630-155">`[CommunicationServiceName <String>]`: CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="20630-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="20630-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20630-157">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="20630-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="20630-158">`[OperationId <String>]`: 진행 중 비동기 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="20630-159">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="20630-160">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="20630-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20630-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="20630-162">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="20630-163">매개 변수: 매개 변수는 액세스 키를 다시 <IRegenerateKeyParameters> 생성하는 요청을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="20630-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="20630-164">`[KeyType <KeyType?>]`: 다시 생성할 keyType입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="20630-165">'primary' 또는 'secondary'(대소문자 무관)입니다.</span><span class="sxs-lookup"><span data-stu-id="20630-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="20630-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20630-166">RELATED LINKS</span></span>

