---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332541"
---
# <span data-ttu-id="ff35d-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="ff35d-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="ff35d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff35d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff35d-103">서비스를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="ff35d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff35d-104">SYNTAX</span></span>

### <span data-ttu-id="ff35d-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff35d-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff35d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff35d-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff35d-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff35d-107">DESCRIPTION</span></span>
<span data-ttu-id="ff35d-108">서비스를 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="ff35d-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff35d-109">EXAMPLES</span></span>

### <span data-ttu-id="ff35d-110">예제 1: 이름으로 Spring Cloud Service를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="ff35d-111">이름으로 Spring Cloud Service를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="ff35d-112">예제 2: 파이프에서 Spring Cloud Service를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="ff35d-113">파이프에서 Spring Cloud Service를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="ff35d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff35d-114">PARAMETERS</span></span>

### <span data-ttu-id="ff35d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff35d-115">-AsJob</span></span>
<span data-ttu-id="ff35d-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ff35d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ff35d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff35d-117">-DefaultProfile</span></span>
<span data-ttu-id="ff35d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff35d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff35d-119">-InputObject</span></span>
<span data-ttu-id="ff35d-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ff35d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff35d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff35d-121">-Name</span></span>
<span data-ttu-id="ff35d-122">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff35d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ff35d-123">-NoWait</span></span>
<span data-ttu-id="ff35d-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ff35d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ff35d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff35d-125">-PassThru</span></span>
<span data-ttu-id="ff35d-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ff35d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff35d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff35d-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ff35d-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ff35d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff35d-130">-SubscriptionId</span></span>
<span data-ttu-id="ff35d-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff35d-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ff35d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff35d-133">-Confirm</span></span>
<span data-ttu-id="ff35d-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff35d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff35d-135">-WhatIf</span></span>
<span data-ttu-id="ff35d-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff35d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff35d-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff35d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff35d-138">CommonParameters</span></span>
<span data-ttu-id="ff35d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff35d-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff35d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff35d-141">입력</span><span class="sxs-lookup"><span data-stu-id="ff35d-141">INPUTS</span></span>

### <span data-ttu-id="ff35d-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ff35d-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ff35d-143">출력</span><span class="sxs-lookup"><span data-stu-id="ff35d-143">OUTPUTS</span></span>

### <span data-ttu-id="ff35d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff35d-144">System.Boolean</span></span>

## <span data-ttu-id="ff35d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff35d-145">NOTES</span></span>

<span data-ttu-id="ff35d-146">별칭</span><span class="sxs-lookup"><span data-stu-id="ff35d-146">ALIASES</span></span>

<span data-ttu-id="ff35d-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ff35d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff35d-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff35d-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff35d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff35d-150">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff35d-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff35d-151">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ff35d-152">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ff35d-153">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ff35d-154">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ff35d-155">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ff35d-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ff35d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff35d-157">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="ff35d-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ff35d-158">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ff35d-159">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ff35d-160">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ff35d-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ff35d-162">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35d-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ff35d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff35d-163">RELATED LINKS</span></span>

