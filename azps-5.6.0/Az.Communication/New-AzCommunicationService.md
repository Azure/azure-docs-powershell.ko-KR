---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991634"
---
# <span data-ttu-id="41e97-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="41e97-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="41e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e97-102">SYNOPSIS</span></span>
<span data-ttu-id="41e97-103">새 CommunicationService를 만들거나 기존 CommunicationService를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="41e97-104">구문</span><span class="sxs-lookup"><span data-stu-id="41e97-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41e97-105">설명</span><span class="sxs-lookup"><span data-stu-id="41e97-105">DESCRIPTION</span></span>
<span data-ttu-id="41e97-106">새 CommunicationService를 만들거나 기존 CommunicationService를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="41e97-107">예제</span><span class="sxs-lookup"><span data-stu-id="41e97-107">EXAMPLES</span></span>

### <span data-ttu-id="41e97-108">예제 1: ACS 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="41e97-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="41e97-109">지정된 매개 변수를 사용하여 ACS 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="41e97-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="41e97-110">PARAMETERS</span></span>

### <span data-ttu-id="41e97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41e97-111">-AsJob</span></span>
<span data-ttu-id="41e97-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-112">Run the command as a job</span></span>

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

### <span data-ttu-id="41e97-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="41e97-113">-DataLocation</span></span>
<span data-ttu-id="41e97-114">통신 서비스에서 해당 데이터를 저장하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="41e97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e97-115">-DefaultProfile</span></span>
<span data-ttu-id="41e97-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e97-117">-Location</span><span class="sxs-lookup"><span data-stu-id="41e97-117">-Location</span></span>
<span data-ttu-id="41e97-118">CommunicationService가 실행되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="41e97-119">-Name</span><span class="sxs-lookup"><span data-stu-id="41e97-119">-Name</span></span>
<span data-ttu-id="41e97-120">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="41e97-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41e97-121">-NoWait</span></span>
<span data-ttu-id="41e97-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="41e97-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41e97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e97-123">-ResourceGroupName</span></span>
<span data-ttu-id="41e97-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="41e97-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="41e97-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41e97-126">-SubscriptionId</span></span>
<span data-ttu-id="41e97-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="41e97-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41e97-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="41e97-129">-Tag</span></span>
<span data-ttu-id="41e97-130">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="41e97-131">-확인</span><span class="sxs-lookup"><span data-stu-id="41e97-131">-Confirm</span></span>
<span data-ttu-id="41e97-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e97-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e97-133">-WhatIf</span></span>
<span data-ttu-id="41e97-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e97-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e97-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e97-136">CommonParameters</span></span>
<span data-ttu-id="41e97-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41e97-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e97-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41e97-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e97-139">입력</span><span class="sxs-lookup"><span data-stu-id="41e97-139">INPUTS</span></span>

## <span data-ttu-id="41e97-140">출력</span><span class="sxs-lookup"><span data-stu-id="41e97-140">OUTPUTS</span></span>

### <span data-ttu-id="41e97-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="41e97-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="41e97-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41e97-142">NOTES</span></span>

<span data-ttu-id="41e97-143">별칭</span><span class="sxs-lookup"><span data-stu-id="41e97-143">ALIASES</span></span>

## <span data-ttu-id="41e97-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41e97-144">RELATED LINKS</span></span>

