---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: c6dccbaa5e398d5d00b02a28cc8942b9e5264859
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977760"
---
# <span data-ttu-id="98469-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="98469-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="98469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98469-102">SYNOPSIS</span></span>
<span data-ttu-id="98469-103">앱을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-103">Operation to delete an App.</span></span>

## <span data-ttu-id="98469-104">구문</span><span class="sxs-lookup"><span data-stu-id="98469-104">SYNTAX</span></span>

### <span data-ttu-id="98469-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="98469-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="98469-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98469-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98469-107">설명</span><span class="sxs-lookup"><span data-stu-id="98469-107">DESCRIPTION</span></span>
<span data-ttu-id="98469-108">앱을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-108">Operation to delete an App.</span></span>

## <span data-ttu-id="98469-109">예제</span><span class="sxs-lookup"><span data-stu-id="98469-109">EXAMPLES</span></span>

### <span data-ttu-id="98469-110">예제 1: 이름에 의해 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="98469-111">이름에 의해 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="98469-112">예제 2: 파이프에서 Spring Cloud App 제거</span><span class="sxs-lookup"><span data-stu-id="98469-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="98469-113">파이프에서 Spring Cloud 앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="98469-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="98469-114">PARAMETERS</span></span>

### <span data-ttu-id="98469-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98469-115">-AsJob</span></span>
<span data-ttu-id="98469-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-116">Run the command as a job</span></span>

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

### <span data-ttu-id="98469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98469-117">-DefaultProfile</span></span>
<span data-ttu-id="98469-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98469-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98469-119">-InputObject</span></span>
<span data-ttu-id="98469-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="98469-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="98469-121">-Name</span><span class="sxs-lookup"><span data-stu-id="98469-121">-Name</span></span>
<span data-ttu-id="98469-122">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98469-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="98469-123">-NoWait</span></span>
<span data-ttu-id="98469-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="98469-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98469-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98469-125">-PassThru</span></span>
<span data-ttu-id="98469-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="98469-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98469-127">-ResourceGroupName</span></span>
<span data-ttu-id="98469-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="98469-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98469-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="98469-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98469-130">-ServiceName</span></span>
<span data-ttu-id="98469-131">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="98469-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98469-132">-SubscriptionId</span></span>
<span data-ttu-id="98469-133">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98469-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="98469-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="98469-135">-확인</span><span class="sxs-lookup"><span data-stu-id="98469-135">-Confirm</span></span>
<span data-ttu-id="98469-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98469-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98469-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98469-137">-WhatIf</span></span>
<span data-ttu-id="98469-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="98469-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98469-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98469-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98469-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98469-140">CommonParameters</span></span>
<span data-ttu-id="98469-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98469-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98469-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98469-143">입력</span><span class="sxs-lookup"><span data-stu-id="98469-143">INPUTS</span></span>

### <span data-ttu-id="98469-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="98469-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="98469-145">출력</span><span class="sxs-lookup"><span data-stu-id="98469-145">OUTPUTS</span></span>

### <span data-ttu-id="98469-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98469-146">System.Boolean</span></span>

## <span data-ttu-id="98469-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98469-147">NOTES</span></span>

<span data-ttu-id="98469-148">별칭</span><span class="sxs-lookup"><span data-stu-id="98469-148">ALIASES</span></span>

<span data-ttu-id="98469-149">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="98469-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98469-150">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98469-151">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98469-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98469-152">INPUTOBJECT <ISpringCloudIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="98469-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98469-153">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="98469-154">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="98469-155">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="98469-156">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="98469-157">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="98469-158">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="98469-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98469-159">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="98469-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="98469-160">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="98469-161">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98469-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="98469-162">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98469-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="98469-163">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98469-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="98469-164">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="98469-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="98469-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98469-165">RELATED LINKS</span></span>

