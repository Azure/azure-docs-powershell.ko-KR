---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195340"
---
# <span data-ttu-id="b8b5d-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="b8b5d-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="b8b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b5d-103">지정된 구성 저장소에 대한 액세스 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="b8b5d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8b5d-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8b5d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b5d-106">지정된 구성 저장소에 대한 액세스 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="b8b5d-107">예제</span><span class="sxs-lookup"><span data-stu-id="b8b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b5d-108">예제 1: 앱 구성 저장소의 모든 저장소 키 나열</span><span class="sxs-lookup"><span data-stu-id="b8b5d-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="b8b5d-109">이 명령은 앱 구성 저장소의 모든 저장소 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="b8b5d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b5d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8b5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b5d-111">-DefaultProfile</span></span>
<span data-ttu-id="b8b5d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b5d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b8b5d-113">-Name</span></span>
<span data-ttu-id="b8b5d-114">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="b8b5d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b5d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8b5d-116">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="b8b5d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8b5d-117">-SubscriptionId</span></span>
<span data-ttu-id="b8b5d-118">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b5d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8b5d-119">-Confirm</span></span>
<span data-ttu-id="b8b5d-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8b5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b5d-121">-WhatIf</span></span>
<span data-ttu-id="b8b5d-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b8b5d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b5d-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8b5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b5d-124">CommonParameters</span></span>
<span data-ttu-id="b8b5d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b5d-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8b5d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b5d-127">입력</span><span class="sxs-lookup"><span data-stu-id="b8b5d-127">INPUTS</span></span>

## <span data-ttu-id="b8b5d-128">출력</span><span class="sxs-lookup"><span data-stu-id="b8b5d-128">OUTPUTS</span></span>

### <span data-ttu-id="b8b5d-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="b8b5d-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="b8b5d-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8b5d-130">NOTES</span></span>

<span data-ttu-id="b8b5d-131">별칭</span><span class="sxs-lookup"><span data-stu-id="b8b5d-131">ALIASES</span></span>

## <span data-ttu-id="b8b5d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8b5d-132">RELATED LINKS</span></span>

