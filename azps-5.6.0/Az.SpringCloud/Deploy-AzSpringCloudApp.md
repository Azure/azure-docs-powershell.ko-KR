---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955328"
---
# <span data-ttu-id="7d92a-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="7d92a-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="7d92a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d92a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d92a-103">서비스에 기본 제공된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="7d92a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d92a-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7d92a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7d92a-105">DESCRIPTION</span></span>
<span data-ttu-id="7d92a-106">서비스에 기본 제공된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="7d92a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7d92a-107">EXAMPLES</span></span>

### <span data-ttu-id="7d92a-108">예제 1: 이름으로 서비스에 로컬 컴파일된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="7d92a-109">이름으로 서비스에 로컬 컴파일된 jar을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="7d92a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d92a-110">PARAMETERS</span></span>

### <span data-ttu-id="7d92a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d92a-111">-AsJob</span></span>
<span data-ttu-id="7d92a-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7d92a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d92a-113">-DefaultProfile</span></span>
<span data-ttu-id="7d92a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d92a-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="7d92a-115">-JarPath</span></span>
<span data-ttu-id="7d92a-116">jar의 경로를 디스로이화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="7d92a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7d92a-117">-Name</span></span>
<span data-ttu-id="7d92a-118">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="7d92a-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7d92a-119">-NoWait</span></span>
<span data-ttu-id="7d92a-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="7d92a-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7d92a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d92a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d92a-122">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7d92a-123">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7d92a-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7d92a-124">-ServiceName</span></span>
<span data-ttu-id="7d92a-125">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7d92a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d92a-126">-SubscriptionId</span></span>
<span data-ttu-id="7d92a-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7d92a-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7d92a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7d92a-129">-Confirm</span></span>
<span data-ttu-id="7d92a-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d92a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d92a-131">-WhatIf</span></span>
<span data-ttu-id="7d92a-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d92a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d92a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d92a-134">CommonParameters</span></span>
<span data-ttu-id="7d92a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d92a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d92a-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d92a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d92a-137">입력</span><span class="sxs-lookup"><span data-stu-id="7d92a-137">INPUTS</span></span>

## <span data-ttu-id="7d92a-138">출력</span><span class="sxs-lookup"><span data-stu-id="7d92a-138">OUTPUTS</span></span>

### <span data-ttu-id="7d92a-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="7d92a-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="7d92a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d92a-140">NOTES</span></span>

<span data-ttu-id="7d92a-141">별칭</span><span class="sxs-lookup"><span data-stu-id="7d92a-141">ALIASES</span></span>

## <span data-ttu-id="7d92a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d92a-142">RELATED LINKS</span></span>

