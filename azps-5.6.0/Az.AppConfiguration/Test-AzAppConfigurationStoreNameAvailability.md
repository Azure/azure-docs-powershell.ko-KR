---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963312"
---
# <span data-ttu-id="793d7-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="793d7-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="793d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="793d7-102">SYNOPSIS</span></span>
<span data-ttu-id="793d7-103">구성 저장소 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="793d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="793d7-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="793d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="793d7-105">DESCRIPTION</span></span>
<span data-ttu-id="793d7-106">구성 저장소 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="793d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="793d7-107">EXAMPLES</span></span>

### <span data-ttu-id="793d7-108">예제 1: 앱 구성 저장소 이름의 가용성 테스트</span><span class="sxs-lookup"><span data-stu-id="793d7-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="793d7-109">이 명령은 앱 구성 저장소 이름의 가용성을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="793d7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="793d7-110">PARAMETERS</span></span>

### <span data-ttu-id="793d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793d7-111">-DefaultProfile</span></span>
<span data-ttu-id="793d7-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="793d7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="793d7-113">-Name</span></span>
<span data-ttu-id="793d7-114">가용성을 확인할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="793d7-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="793d7-115">-SubscriptionId</span></span>
<span data-ttu-id="793d7-116">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="793d7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="793d7-117">-Confirm</span></span>
<span data-ttu-id="793d7-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793d7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793d7-119">-WhatIf</span></span>
<span data-ttu-id="793d7-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="793d7-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793d7-122">CommonParameters</span></span>
<span data-ttu-id="793d7-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="793d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793d7-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="793d7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793d7-125">입력</span><span class="sxs-lookup"><span data-stu-id="793d7-125">INPUTS</span></span>

## <span data-ttu-id="793d7-126">출력</span><span class="sxs-lookup"><span data-stu-id="793d7-126">OUTPUTS</span></span>

### <span data-ttu-id="793d7-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="793d7-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="793d7-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="793d7-128">NOTES</span></span>

<span data-ttu-id="793d7-129">별칭</span><span class="sxs-lookup"><span data-stu-id="793d7-129">ALIASES</span></span>

## <span data-ttu-id="793d7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="793d7-130">RELATED LINKS</span></span>

