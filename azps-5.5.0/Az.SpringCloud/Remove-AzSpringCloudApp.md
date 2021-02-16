---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201548"
---
# <span data-ttu-id="6d5da-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="6d5da-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="6d5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5da-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5da-103">앱을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-103">Operation to delete an App.</span></span>

## <span data-ttu-id="6d5da-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d5da-104">SYNTAX</span></span>

### <span data-ttu-id="6d5da-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="6d5da-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6d5da-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5da-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d5da-107">설명</span><span class="sxs-lookup"><span data-stu-id="6d5da-107">DESCRIPTION</span></span>
<span data-ttu-id="6d5da-108">앱을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-108">Operation to delete an App.</span></span>

## <span data-ttu-id="6d5da-109">예제</span><span class="sxs-lookup"><span data-stu-id="6d5da-109">EXAMPLES</span></span>

### <span data-ttu-id="6d5da-110">예제 1: 이름으로 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="6d5da-111">이름으로 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="6d5da-112">예제 2: 파이프에서 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="6d5da-113">파이프에서 Spring Cloud App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="6d5da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5da-114">PARAMETERS</span></span>

### <span data-ttu-id="6d5da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d5da-115">-AsJob</span></span>
<span data-ttu-id="6d5da-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="6d5da-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6d5da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5da-117">-DefaultProfile</span></span>
<span data-ttu-id="6d5da-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5da-119">-InputObject</span></span>
<span data-ttu-id="6d5da-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6d5da-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d5da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5da-121">-Name</span></span>
<span data-ttu-id="6d5da-122">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-122">The name of the App resource.</span></span>

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

### <span data-ttu-id="6d5da-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6d5da-123">-NoWait</span></span>
<span data-ttu-id="6d5da-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="6d5da-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6d5da-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d5da-125">-PassThru</span></span>
<span data-ttu-id="6d5da-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6d5da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5da-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d5da-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6d5da-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6d5da-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6d5da-130">-ServiceName</span></span>
<span data-ttu-id="6d5da-131">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="6d5da-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d5da-132">-SubscriptionId</span></span>
<span data-ttu-id="6d5da-133">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d5da-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d5da-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d5da-135">-Confirm</span></span>
<span data-ttu-id="6d5da-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5da-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5da-137">-WhatIf</span></span>
<span data-ttu-id="6d5da-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6d5da-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5da-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5da-140">CommonParameters</span></span>
<span data-ttu-id="6d5da-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5da-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d5da-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5da-143">입력</span><span class="sxs-lookup"><span data-stu-id="6d5da-143">INPUTS</span></span>

### <span data-ttu-id="6d5da-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6d5da-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6d5da-145">출력</span><span class="sxs-lookup"><span data-stu-id="6d5da-145">OUTPUTS</span></span>

### <span data-ttu-id="6d5da-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d5da-146">System.Boolean</span></span>

## <span data-ttu-id="6d5da-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d5da-147">NOTES</span></span>

<span data-ttu-id="6d5da-148">별칭</span><span class="sxs-lookup"><span data-stu-id="6d5da-148">ALIASES</span></span>

<span data-ttu-id="6d5da-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6d5da-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d5da-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d5da-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d5da-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d5da-152">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d5da-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d5da-153">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6d5da-154">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6d5da-155">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6d5da-156">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6d5da-157">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6d5da-158">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6d5da-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d5da-159">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="6d5da-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6d5da-160">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6d5da-161">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6d5da-162">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6d5da-163">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6d5da-164">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5da-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6d5da-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d5da-165">RELATED LINKS</span></span>

