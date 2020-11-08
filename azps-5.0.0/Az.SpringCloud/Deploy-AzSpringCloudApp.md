---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215245"
---
# <span data-ttu-id="ef4f5-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ef4f5-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="ef4f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4f5-103">빌드된 jar를 서비스에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="ef4f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef4f5-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ef4f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef4f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4f5-106">빌드된 jar를 서비스에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="ef4f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef4f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4f5-108">예제 1: 이름별로 컴파일된 로컬 jar를 서비스에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="ef4f5-109">이름을 기준으로 서비스에 컴파일된 로컬 jar를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="ef4f5-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef4f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4f5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef4f5-111">-AsJob</span></span>
<span data-ttu-id="ef4f5-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ef4f5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ef4f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4f5-113">-DefaultProfile</span></span>
<span data-ttu-id="ef4f5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4f5-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="ef4f5-115">-JarPath</span></span>
<span data-ttu-id="ef4f5-116">Jar 경로를 deploied 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="ef4f5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ef4f5-117">-Name</span></span>
<span data-ttu-id="ef4f5-118">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="ef4f5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef4f5-119">-NoWait</span></span>
<span data-ttu-id="ef4f5-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ef4f5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef4f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef4f5-122">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ef4f5-123">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ef4f5-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ef4f5-124">-ServiceName</span></span>
<span data-ttu-id="ef4f5-125">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ef4f5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef4f5-126">-SubscriptionId</span></span>
<span data-ttu-id="ef4f5-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef4f5-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef4f5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ef4f5-129">-Confirm</span></span>
<span data-ttu-id="ef4f5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4f5-131">-WhatIf</span></span>
<span data-ttu-id="ef4f5-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4f5-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4f5-134">CommonParameters</span></span>
<span data-ttu-id="ef4f5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4f5-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef4f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4f5-137">입력</span><span class="sxs-lookup"><span data-stu-id="ef4f5-137">INPUTS</span></span>

## <span data-ttu-id="ef4f5-138">출력</span><span class="sxs-lookup"><span data-stu-id="ef4f5-138">OUTPUTS</span></span>

### <span data-ttu-id="ef4f5-139">SpringCloud. PowerShell. Api20200701. Iap보도 Ource</span><span class="sxs-lookup"><span data-stu-id="ef4f5-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="ef4f5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ef4f5-140">NOTES</span></span>

<span data-ttu-id="ef4f5-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="ef4f5-141">ALIASES</span></span>

## <span data-ttu-id="ef4f5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef4f5-142">RELATED LINKS</span></span>

