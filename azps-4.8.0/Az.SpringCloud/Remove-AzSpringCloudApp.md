---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213928"
---
# <span data-ttu-id="afa47-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="afa47-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="afa47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa47-102">SYNOPSIS</span></span>
<span data-ttu-id="afa47-103">앱을 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-103">Operation to delete an App.</span></span>

## <span data-ttu-id="afa47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afa47-104">SYNTAX</span></span>

### <span data-ttu-id="afa47-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="afa47-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="afa47-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="afa47-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afa47-107">설명은</span><span class="sxs-lookup"><span data-stu-id="afa47-107">DESCRIPTION</span></span>
<span data-ttu-id="afa47-108">앱을 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-108">Operation to delete an App.</span></span>

## <span data-ttu-id="afa47-109">예제의</span><span class="sxs-lookup"><span data-stu-id="afa47-109">EXAMPLES</span></span>

### <span data-ttu-id="afa47-110">예제 1: 이름으로 스프링 클라우드 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="afa47-111">이름으로 스프링 클라우드 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="afa47-112">예제 2: 파이프에서 스프링 클라우드 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="afa47-113">파이프에서 스프링 클라우드 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="afa47-114">변수</span><span class="sxs-lookup"><span data-stu-id="afa47-114">PARAMETERS</span></span>

### <span data-ttu-id="afa47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa47-115">-DefaultProfile</span></span>
<span data-ttu-id="afa47-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa47-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afa47-117">-InputObject</span></span>
<span data-ttu-id="afa47-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="afa47-119">-이름</span><span class="sxs-lookup"><span data-stu-id="afa47-119">-Name</span></span>
<span data-ttu-id="afa47-120">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-120">The name of the App resource.</span></span>

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

### <span data-ttu-id="afa47-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afa47-121">-PassThru</span></span>
<span data-ttu-id="afa47-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="afa47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa47-123">-ResourceGroupName</span></span>
<span data-ttu-id="afa47-124">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="afa47-125">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="afa47-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="afa47-126">-ServiceName</span></span>
<span data-ttu-id="afa47-127">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="afa47-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afa47-128">-SubscriptionId</span></span>
<span data-ttu-id="afa47-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="afa47-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="afa47-131">-확인</span><span class="sxs-lookup"><span data-stu-id="afa47-131">-Confirm</span></span>
<span data-ttu-id="afa47-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa47-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa47-133">-WhatIf</span></span>
<span data-ttu-id="afa47-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa47-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa47-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa47-136">CommonParameters</span></span>
<span data-ttu-id="afa47-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa47-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="afa47-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa47-139">입력</span><span class="sxs-lookup"><span data-stu-id="afa47-139">INPUTS</span></span>

### <span data-ttu-id="afa47-140">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="afa47-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="afa47-141">출력</span><span class="sxs-lookup"><span data-stu-id="afa47-141">OUTPUTS</span></span>

### <span data-ttu-id="afa47-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="afa47-142">System.Boolean</span></span>

## <span data-ttu-id="afa47-143">상속자</span><span class="sxs-lookup"><span data-stu-id="afa47-143">NOTES</span></span>

<span data-ttu-id="afa47-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="afa47-144">ALIASES</span></span>

<span data-ttu-id="afa47-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="afa47-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="afa47-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afa47-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="afa47-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="afa47-148">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="afa47-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="afa47-149">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="afa47-150">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="afa47-151">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="afa47-152">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="afa47-153">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="afa47-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="afa47-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="afa47-155">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="afa47-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="afa47-156">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="afa47-157">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="afa47-158">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="afa47-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="afa47-160">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afa47-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="afa47-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afa47-161">RELATED LINKS</span></span>

