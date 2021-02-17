---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207984"
---
# <span data-ttu-id="24cb7-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="24cb7-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="24cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="24cb7-103">서비스에 기본 제공 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="24cb7-104">구문</span><span class="sxs-lookup"><span data-stu-id="24cb7-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="24cb7-105">설명</span><span class="sxs-lookup"><span data-stu-id="24cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="24cb7-106">서비스에 기본 제공 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="24cb7-107">예제</span><span class="sxs-lookup"><span data-stu-id="24cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="24cb7-108">예제 1: 이름으로 서비스에 로컬 컴파일된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="24cb7-109">이름으로 서비스에 로컬 컴파일된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="24cb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24cb7-110">PARAMETERS</span></span>

### <span data-ttu-id="24cb7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24cb7-111">-AsJob</span></span>
<span data-ttu-id="24cb7-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="24cb7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="24cb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cb7-113">-DefaultProfile</span></span>
<span data-ttu-id="24cb7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cb7-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="24cb7-115">-JarPath</span></span>
<span data-ttu-id="24cb7-116">jar의 경로를 디포이트해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="24cb7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24cb7-117">-Name</span></span>
<span data-ttu-id="24cb7-118">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="24cb7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24cb7-119">-NoWait</span></span>
<span data-ttu-id="24cb7-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="24cb7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="24cb7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cb7-121">-ResourceGroupName</span></span>
<span data-ttu-id="24cb7-122">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="24cb7-123">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="24cb7-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="24cb7-124">-ServiceName</span></span>
<span data-ttu-id="24cb7-125">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="24cb7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24cb7-126">-SubscriptionId</span></span>
<span data-ttu-id="24cb7-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="24cb7-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24cb7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24cb7-129">-Confirm</span></span>
<span data-ttu-id="24cb7-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cb7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cb7-131">-WhatIf</span></span>
<span data-ttu-id="24cb7-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="24cb7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cb7-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cb7-134">CommonParameters</span></span>
<span data-ttu-id="24cb7-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24cb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cb7-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24cb7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cb7-137">입력</span><span class="sxs-lookup"><span data-stu-id="24cb7-137">INPUTS</span></span>

## <span data-ttu-id="24cb7-138">출력</span><span class="sxs-lookup"><span data-stu-id="24cb7-138">OUTPUTS</span></span>

### <span data-ttu-id="24cb7-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="24cb7-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="24cb7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24cb7-140">NOTES</span></span>

<span data-ttu-id="24cb7-141">별칭</span><span class="sxs-lookup"><span data-stu-id="24cb7-141">ALIASES</span></span>

## <span data-ttu-id="24cb7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24cb7-142">RELATED LINKS</span></span>

