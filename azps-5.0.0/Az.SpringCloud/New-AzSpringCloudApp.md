---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215237"
---
# <span data-ttu-id="9870e-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="9870e-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="9870e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9870e-102">SYNOPSIS</span></span>
<span data-ttu-id="9870e-103">새 앱을 만들거나 종료 하는 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="9870e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9870e-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9870e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9870e-105">DESCRIPTION</span></span>
<span data-ttu-id="9870e-106">새 앱을 만들거나 종료 하는 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="9870e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9870e-107">EXAMPLES</span></span>

### <span data-ttu-id="9870e-108">예제 1: 스프링 클라우드 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="9870e-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="9870e-109">스프링 클라우드 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="9870e-110">변수</span><span class="sxs-lookup"><span data-stu-id="9870e-110">PARAMETERS</span></span>

### <span data-ttu-id="9870e-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="9870e-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="9870e-112">앱의 활성 배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="9870e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9870e-113">-AsJob</span></span>
<span data-ttu-id="9870e-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9870e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9870e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9870e-115">-DefaultProfile</span></span>
<span data-ttu-id="9870e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9870e-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="9870e-117">-Fqdn</span></span>
<span data-ttu-id="9870e-118">정규화 된 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="9870e-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9870e-119">-HttpsOnly</span></span>
<span data-ttu-id="9870e-120">Https만 허용 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="9870e-121">-위치</span><span class="sxs-lookup"><span data-stu-id="9870e-121">-Location</span></span>
<span data-ttu-id="9870e-122">응용 프로그램의 지리적 위치 이며 항상 부모 리소스와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="9870e-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9870e-123">-Name</span></span>
<span data-ttu-id="9870e-124">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="9870e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9870e-125">-NoWait</span></span>
<span data-ttu-id="9870e-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9870e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9870e-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="9870e-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="9870e-128">영구 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="9870e-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="9870e-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="9870e-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="9870e-130">영구 디스크의 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="9870e-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="9870e-131">-공용</span><span class="sxs-lookup"><span data-stu-id="9870e-131">-Public</span></span>
<span data-ttu-id="9870e-132">앱이 공개 끝점을 노출 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="9870e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9870e-133">-ResourceGroupName</span></span>
<span data-ttu-id="9870e-134">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9870e-135">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9870e-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9870e-136">-ServiceName</span></span>
<span data-ttu-id="9870e-137">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="9870e-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9870e-138">-SubscriptionId</span></span>
<span data-ttu-id="9870e-139">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9870e-140">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9870e-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="9870e-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="9870e-142">임시 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="9870e-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="9870e-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="9870e-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="9870e-144">임시 디스크 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="9870e-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="9870e-145">-확인</span><span class="sxs-lookup"><span data-stu-id="9870e-145">-Confirm</span></span>
<span data-ttu-id="9870e-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9870e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9870e-147">-WhatIf</span></span>
<span data-ttu-id="9870e-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9870e-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9870e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9870e-150">CommonParameters</span></span>
<span data-ttu-id="9870e-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9870e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9870e-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9870e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9870e-153">입력</span><span class="sxs-lookup"><span data-stu-id="9870e-153">INPUTS</span></span>

## <span data-ttu-id="9870e-154">출력</span><span class="sxs-lookup"><span data-stu-id="9870e-154">OUTPUTS</span></span>

### <span data-ttu-id="9870e-155">SpringCloud. PowerShell. Api20200701. Iap보도 Ource</span><span class="sxs-lookup"><span data-stu-id="9870e-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="9870e-156">상속자</span><span class="sxs-lookup"><span data-stu-id="9870e-156">NOTES</span></span>

<span data-ttu-id="9870e-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="9870e-157">ALIASES</span></span>

## <span data-ttu-id="9870e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9870e-158">RELATED LINKS</span></span>

