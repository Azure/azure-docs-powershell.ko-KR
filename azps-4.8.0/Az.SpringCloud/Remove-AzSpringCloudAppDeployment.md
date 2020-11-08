---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056980"
---
# <span data-ttu-id="c5042-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c5042-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c5042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5042-102">SYNOPSIS</span></span>
<span data-ttu-id="c5042-103">배포를 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="c5042-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5042-104">SYNTAX</span></span>

### <span data-ttu-id="c5042-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5042-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c5042-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5042-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5042-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c5042-107">DESCRIPTION</span></span>
<span data-ttu-id="c5042-108">배포를 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="c5042-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5042-109">EXAMPLES</span></span>

### <span data-ttu-id="c5042-110">예제 1: 이름으로 스프링 클라우드 배포 제거</span><span class="sxs-lookup"><span data-stu-id="c5042-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="c5042-111">이름에 따라 스프링 클라우드 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="c5042-112">예제 2: 파이프에서 스프링 구름 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="c5042-113">파이프에서 스프링 클라우드 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="c5042-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5042-114">PARAMETERS</span></span>

### <span data-ttu-id="c5042-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="c5042-115">-AppName</span></span>
<span data-ttu-id="c5042-116">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="c5042-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5042-117">-DefaultProfile</span></span>
<span data-ttu-id="c5042-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5042-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5042-119">-InputObject</span></span>
<span data-ttu-id="c5042-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5042-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c5042-121">-Name</span></span>
<span data-ttu-id="c5042-122">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-122">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5042-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5042-123">-PassThru</span></span>
<span data-ttu-id="c5042-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c5042-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5042-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5042-126">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c5042-127">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5042-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5042-128">-ServiceName</span></span>
<span data-ttu-id="c5042-129">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c5042-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5042-130">-SubscriptionId</span></span>
<span data-ttu-id="c5042-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5042-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c5042-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c5042-133">-Confirm</span></span>
<span data-ttu-id="c5042-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5042-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5042-135">-WhatIf</span></span>
<span data-ttu-id="c5042-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5042-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5042-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5042-138">CommonParameters</span></span>
<span data-ttu-id="c5042-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5042-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5042-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5042-141">입력</span><span class="sxs-lookup"><span data-stu-id="c5042-141">INPUTS</span></span>

### <span data-ttu-id="c5042-142">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5042-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c5042-143">출력</span><span class="sxs-lookup"><span data-stu-id="c5042-143">OUTPUTS</span></span>

### <span data-ttu-id="c5042-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c5042-144">System.Boolean</span></span>

## <span data-ttu-id="c5042-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c5042-145">NOTES</span></span>

<span data-ttu-id="c5042-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="c5042-146">ALIASES</span></span>

<span data-ttu-id="c5042-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c5042-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5042-148">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5042-149">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5042-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5042-150">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5042-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5042-151">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c5042-152">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c5042-153">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c5042-154">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c5042-155">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c5042-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c5042-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5042-157">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="c5042-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c5042-158">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c5042-159">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c5042-160">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c5042-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c5042-162">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5042-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c5042-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5042-163">RELATED LINKS</span></span>

