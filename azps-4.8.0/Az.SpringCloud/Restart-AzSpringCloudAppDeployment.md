---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 859ea1febad82dbb09e88debe3f825feab18b1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204318"
---
# <span data-ttu-id="fc711-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="fc711-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="fc711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc711-102">SYNOPSIS</span></span>
<span data-ttu-id="fc711-103">배포를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-103">Restart the deployment.</span></span>

## <span data-ttu-id="fc711-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc711-104">SYNTAX</span></span>

### <span data-ttu-id="fc711-105">다시 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc711-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc711-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc711-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc711-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc711-107">DESCRIPTION</span></span>
<span data-ttu-id="fc711-108">배포를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-108">Restart the deployment.</span></span>

## <span data-ttu-id="fc711-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc711-109">EXAMPLES</span></span>

### <span data-ttu-id="fc711-110">예제 1: 이름으로 스프링 클라우드 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="fc711-111">이름으로 스프링 클라우드 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="fc711-112">예제 2: 파이프에서 스프링 클라우드 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="fc711-113">파이프에서 스프링 클라우드 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="fc711-114">변수</span><span class="sxs-lookup"><span data-stu-id="fc711-114">PARAMETERS</span></span>

### <span data-ttu-id="fc711-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="fc711-115">-AppName</span></span>
<span data-ttu-id="fc711-116">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc711-117">-AsJob</span></span>
<span data-ttu-id="fc711-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fc711-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fc711-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc711-119">-DefaultProfile</span></span>
<span data-ttu-id="fc711-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc711-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc711-121">-InputObject</span></span>
<span data-ttu-id="fc711-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fc711-123">-Name</span></span>
<span data-ttu-id="fc711-124">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fc711-125">-NoWait</span></span>
<span data-ttu-id="fc711-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fc711-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fc711-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc711-127">-PassThru</span></span>
<span data-ttu-id="fc711-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fc711-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc711-129">-ResourceGroupName</span></span>
<span data-ttu-id="fc711-130">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fc711-131">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fc711-132">-ServiceName</span></span>
<span data-ttu-id="fc711-133">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc711-134">-SubscriptionId</span></span>
<span data-ttu-id="fc711-135">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fc711-136">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc711-137">-확인</span><span class="sxs-lookup"><span data-stu-id="fc711-137">-Confirm</span></span>
<span data-ttu-id="fc711-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc711-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc711-139">-WhatIf</span></span>
<span data-ttu-id="fc711-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc711-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc711-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc711-142">CommonParameters</span></span>
<span data-ttu-id="fc711-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc711-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc711-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc711-145">입력</span><span class="sxs-lookup"><span data-stu-id="fc711-145">INPUTS</span></span>

### <span data-ttu-id="fc711-146">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc711-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="fc711-147">출력</span><span class="sxs-lookup"><span data-stu-id="fc711-147">OUTPUTS</span></span>

### <span data-ttu-id="fc711-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fc711-148">System.Boolean</span></span>

## <span data-ttu-id="fc711-149">상속자</span><span class="sxs-lookup"><span data-stu-id="fc711-149">NOTES</span></span>

<span data-ttu-id="fc711-150">별칭과</span><span class="sxs-lookup"><span data-stu-id="fc711-150">ALIASES</span></span>

<span data-ttu-id="fc711-151">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="fc711-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc711-152">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc711-153">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc711-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc711-154">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc711-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc711-155">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="fc711-156">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="fc711-157">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="fc711-158">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="fc711-159">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="fc711-160">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="fc711-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc711-161">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="fc711-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="fc711-162">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fc711-163">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fc711-164">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="fc711-165">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="fc711-166">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc711-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fc711-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc711-167">RELATED LINKS</span></span>

