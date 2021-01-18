---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494724"
---
# <span data-ttu-id="afe13-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="afe13-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="afe13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe13-102">SYNOPSIS</span></span>
<span data-ttu-id="afe13-103">새 앱을 만들거나 종료하는 앱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="afe13-104">구문</span><span class="sxs-lookup"><span data-stu-id="afe13-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afe13-105">설명</span><span class="sxs-lookup"><span data-stu-id="afe13-105">DESCRIPTION</span></span>
<span data-ttu-id="afe13-106">새 앱을 만들거나 종료하는 앱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="afe13-107">예제</span><span class="sxs-lookup"><span data-stu-id="afe13-107">EXAMPLES</span></span>

### <span data-ttu-id="afe13-108">예제 1: Spring Cloud 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="afe13-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="afe13-109">Spring Cloud 앱을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="afe13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afe13-110">PARAMETERS</span></span>

### <span data-ttu-id="afe13-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="afe13-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="afe13-112">앱의 활성 배포 이름</span><span class="sxs-lookup"><span data-stu-id="afe13-112">Name of the active deployment of the App</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afe13-113">-AsJob</span></span>
<span data-ttu-id="afe13-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="afe13-114">Run the command as a job</span></span>

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

### <span data-ttu-id="afe13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe13-115">-DefaultProfile</span></span>
<span data-ttu-id="afe13-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe13-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="afe13-117">-Fqdn</span></span>
<span data-ttu-id="afe13-118">정식 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-118">Fully qualified dns Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="afe13-119">-HttpsOnly</span></span>
<span data-ttu-id="afe13-120">https만 허용되는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="afe13-121">-Location</span><span class="sxs-lookup"><span data-stu-id="afe13-121">-Location</span></span>
<span data-ttu-id="afe13-122">애플리케이션의 GEO 위치( 항상 부모 리소스와 동일)</span><span class="sxs-lookup"><span data-stu-id="afe13-122">The GEO location of the application, always the same with its parent resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-123">-Name</span><span class="sxs-lookup"><span data-stu-id="afe13-123">-Name</span></span>
<span data-ttu-id="afe13-124">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="afe13-125">-NoWait</span></span>
<span data-ttu-id="afe13-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="afe13-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="afe13-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="afe13-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="afe13-128">영구 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="afe13-128">Mount path of the persistent disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="afe13-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="afe13-130">영구 디스크의 크기(GB)</span><span class="sxs-lookup"><span data-stu-id="afe13-130">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-131">-Public</span><span class="sxs-lookup"><span data-stu-id="afe13-131">-Public</span></span>
<span data-ttu-id="afe13-132">앱이 공용 엔드포인트를 노출하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="afe13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe13-133">-ResourceGroupName</span></span>
<span data-ttu-id="afe13-134">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="afe13-135">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="afe13-136">-ServiceName</span></span>
<span data-ttu-id="afe13-137">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afe13-138">-SubscriptionId</span></span>
<span data-ttu-id="afe13-139">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="afe13-140">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="afe13-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="afe13-142">임시 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="afe13-142">Mount path of the temporary disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="afe13-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="afe13-144">임시 디스크의 크기(GB)</span><span class="sxs-lookup"><span data-stu-id="afe13-144">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe13-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afe13-145">-Confirm</span></span>
<span data-ttu-id="afe13-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe13-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe13-147">-WhatIf</span></span>
<span data-ttu-id="afe13-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="afe13-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe13-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe13-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe13-150">CommonParameters</span></span>
<span data-ttu-id="afe13-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="afe13-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe13-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="afe13-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe13-153">입력</span><span class="sxs-lookup"><span data-stu-id="afe13-153">INPUTS</span></span>

## <span data-ttu-id="afe13-154">출력</span><span class="sxs-lookup"><span data-stu-id="afe13-154">OUTPUTS</span></span>

### <span data-ttu-id="afe13-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="afe13-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="afe13-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="afe13-156">NOTES</span></span>

<span data-ttu-id="afe13-157">별칭</span><span class="sxs-lookup"><span data-stu-id="afe13-157">ALIASES</span></span>

## <span data-ttu-id="afe13-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afe13-158">RELATED LINKS</span></span>

