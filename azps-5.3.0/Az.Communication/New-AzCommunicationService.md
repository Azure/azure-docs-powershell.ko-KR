---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496132"
---
# <span data-ttu-id="6f304-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="6f304-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="6f304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f304-102">SYNOPSIS</span></span>
<span data-ttu-id="6f304-103">새 CommunicationService를 만들거나 기존 CommunicationService를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="6f304-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f304-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f304-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f304-105">DESCRIPTION</span></span>
<span data-ttu-id="6f304-106">새 CommunicationService를 만들거나 기존 CommunicationService를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="6f304-107">예제</span><span class="sxs-lookup"><span data-stu-id="6f304-107">EXAMPLES</span></span>

### <span data-ttu-id="6f304-108">예제 1: ACS 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="6f304-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="6f304-109">지정된 매개 변수를 사용하여 ACS 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="6f304-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f304-110">PARAMETERS</span></span>

### <span data-ttu-id="6f304-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f304-111">-AsJob</span></span>
<span data-ttu-id="6f304-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="6f304-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6f304-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="6f304-113">-DataLocation</span></span>
<span data-ttu-id="6f304-114">통신 서비스가 해당 데이터를 저장하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="6f304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f304-115">-DefaultProfile</span></span>
<span data-ttu-id="6f304-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f304-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6f304-117">-Location</span></span>
<span data-ttu-id="6f304-118">CommunicationService가 실행되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="6f304-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6f304-119">-Name</span></span>
<span data-ttu-id="6f304-120">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f304-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6f304-121">-NoWait</span></span>
<span data-ttu-id="6f304-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="6f304-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6f304-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f304-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f304-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6f304-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6f304-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f304-126">-SubscriptionId</span></span>
<span data-ttu-id="6f304-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6f304-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6f304-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f304-129">-Tag</span></span>
<span data-ttu-id="6f304-130">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f304-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f304-131">-Confirm</span></span>
<span data-ttu-id="6f304-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f304-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f304-133">-WhatIf</span></span>
<span data-ttu-id="6f304-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6f304-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f304-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f304-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f304-136">CommonParameters</span></span>
<span data-ttu-id="6f304-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f304-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f304-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f304-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f304-139">입력</span><span class="sxs-lookup"><span data-stu-id="6f304-139">INPUTS</span></span>

## <span data-ttu-id="6f304-140">출력</span><span class="sxs-lookup"><span data-stu-id="6f304-140">OUTPUTS</span></span>

### <span data-ttu-id="6f304-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="6f304-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="6f304-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f304-142">NOTES</span></span>

<span data-ttu-id="6f304-143">별칭</span><span class="sxs-lookup"><span data-stu-id="6f304-143">ALIASES</span></span>

## <span data-ttu-id="6f304-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f304-144">RELATED LINKS</span></span>

