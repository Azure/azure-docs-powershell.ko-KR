---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4ffb65d4eca9511e179d33c53cb8f515c28aab58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205080"
---
# <span data-ttu-id="8c9b2-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8c9b2-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="8c9b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9b2-103">지정된 업데이트 도메인에서 역할 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="8c9b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c9b2-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8c9b2-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="8c9b2-106">지정된 업데이트 도메인에서 역할 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="8c9b2-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c9b2-107">EXAMPLES</span></span>

### <span data-ttu-id="8c9b2-108">예제 1: 업데이트 도메인에서 역할 인스턴스 업데이트</span><span class="sxs-lookup"><span data-stu-id="8c9b2-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="8c9b2-109">이 명령은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스의 업데이트 도메인 0에서 역할 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8c9b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c9b2-110">PARAMETERS</span></span>

### <span data-ttu-id="8c9b2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c9b2-111">-AsJob</span></span>
<span data-ttu-id="8c9b2-112">명령 실행</span><span class="sxs-lookup"><span data-stu-id="8c9b2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8c9b2-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="8c9b2-113">-CloudServiceName</span></span>
<span data-ttu-id="8c9b2-114">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="8c9b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9b2-115">-DefaultProfile</span></span>
<span data-ttu-id="8c9b2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c9b2-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8c9b2-117">-NoWait</span></span>
<span data-ttu-id="8c9b2-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="8c9b2-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c9b2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c9b2-119">-PassThru</span></span>
<span data-ttu-id="8c9b2-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c9b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c9b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c9b2-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="8c9b2-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c9b2-123">-SubscriptionId</span></span>
<span data-ttu-id="8c9b2-124">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c9b2-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8c9b2-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8c9b2-126">-UpdateDomain</span></span>
<span data-ttu-id="8c9b2-127">업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="8c9b2-128">업데이트 도메인은 0부터 시작하여 식별됩니다. 첫 번째 업데이트 도메인의 ID는 0이고, 두 번째 도메인은 ID가 1인 등입니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c9b2-129">-Confirm</span></span>
<span data-ttu-id="8c9b2-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c9b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c9b2-131">-WhatIf</span></span>
<span data-ttu-id="8c9b2-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8c9b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c9b2-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c9b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9b2-134">CommonParameters</span></span>
<span data-ttu-id="8c9b2-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9b2-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c9b2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9b2-137">입력</span><span class="sxs-lookup"><span data-stu-id="8c9b2-137">INPUTS</span></span>

## <span data-ttu-id="8c9b2-138">출력</span><span class="sxs-lookup"><span data-stu-id="8c9b2-138">OUTPUTS</span></span>

### <span data-ttu-id="8c9b2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c9b2-139">System.Boolean</span></span>

## <span data-ttu-id="8c9b2-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c9b2-140">NOTES</span></span>

<span data-ttu-id="8c9b2-141">별칭</span><span class="sxs-lookup"><span data-stu-id="8c9b2-141">ALIASES</span></span>

## <span data-ttu-id="8c9b2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c9b2-142">RELATED LINKS</span></span>

