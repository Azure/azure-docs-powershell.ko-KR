---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213929"
---
# <span data-ttu-id="82f5b-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="82f5b-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="82f5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="82f5b-103">서비스를 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="82f5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82f5b-104">SYNTAX</span></span>

### <span data-ttu-id="82f5b-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="82f5b-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="82f5b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="82f5b-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82f5b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="82f5b-107">DESCRIPTION</span></span>
<span data-ttu-id="82f5b-108">서비스를 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="82f5b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="82f5b-109">EXAMPLES</span></span>

### <span data-ttu-id="82f5b-110">예제 1: 이름으로 스프링 클라우드 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="82f5b-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="82f5b-111">이름으로 스프링 클라우드 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="82f5b-112">예제 2: 파이프에서 스프링 클라우드 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="82f5b-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="82f5b-113">파이프에서 스프링 클라우드 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="82f5b-114">변수</span><span class="sxs-lookup"><span data-stu-id="82f5b-114">PARAMETERS</span></span>

### <span data-ttu-id="82f5b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82f5b-115">-AsJob</span></span>
<span data-ttu-id="82f5b-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="82f5b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="82f5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f5b-117">-DefaultProfile</span></span>
<span data-ttu-id="82f5b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82f5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82f5b-119">-InputObject</span></span>
<span data-ttu-id="82f5b-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82f5b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="82f5b-121">-Name</span></span>
<span data-ttu-id="82f5b-122">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="82f5b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82f5b-123">-NoWait</span></span>
<span data-ttu-id="82f5b-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="82f5b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="82f5b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82f5b-125">-PassThru</span></span>
<span data-ttu-id="82f5b-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="82f5b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f5b-127">-ResourceGroupName</span></span>
<span data-ttu-id="82f5b-128">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="82f5b-129">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="82f5b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82f5b-130">-SubscriptionId</span></span>
<span data-ttu-id="82f5b-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="82f5b-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="82f5b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="82f5b-133">-Confirm</span></span>
<span data-ttu-id="82f5b-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f5b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f5b-135">-WhatIf</span></span>
<span data-ttu-id="82f5b-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82f5b-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f5b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f5b-138">CommonParameters</span></span>
<span data-ttu-id="82f5b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f5b-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82f5b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f5b-141">입력</span><span class="sxs-lookup"><span data-stu-id="82f5b-141">INPUTS</span></span>

### <span data-ttu-id="82f5b-142">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="82f5b-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="82f5b-143">출력</span><span class="sxs-lookup"><span data-stu-id="82f5b-143">OUTPUTS</span></span>

### <span data-ttu-id="82f5b-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="82f5b-144">System.Boolean</span></span>

## <span data-ttu-id="82f5b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="82f5b-145">NOTES</span></span>

<span data-ttu-id="82f5b-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="82f5b-146">ALIASES</span></span>

<span data-ttu-id="82f5b-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="82f5b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82f5b-148">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82f5b-149">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="82f5b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82f5b-150">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="82f5b-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="82f5b-151">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="82f5b-152">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="82f5b-153">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="82f5b-154">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="82f5b-155">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="82f5b-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="82f5b-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="82f5b-157">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="82f5b-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="82f5b-158">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="82f5b-159">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="82f5b-160">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="82f5b-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="82f5b-162">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="82f5b-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="82f5b-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82f5b-163">RELATED LINKS</span></span>

