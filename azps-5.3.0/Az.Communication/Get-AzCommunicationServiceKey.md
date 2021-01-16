---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493929"
---
# <span data-ttu-id="1ffe7-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="1ffe7-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="1ffe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffe7-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffe7-103">CommunicationService 리소스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="1ffe7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ffe7-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ffe7-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ffe7-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffe7-106">CommunicationService 리소스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="1ffe7-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ffe7-107">EXAMPLES</span></span>

### <span data-ttu-id="1ffe7-108">예제 1: 지정된 통신 서비스에 대한 키 페치</span><span class="sxs-lookup"><span data-stu-id="1ffe7-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="1ffe7-109">지정된 통신 서비스에 대한 ConnectionString 및 키를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="1ffe7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ffe7-110">PARAMETERS</span></span>

### <span data-ttu-id="1ffe7-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="1ffe7-111">-CommunicationServiceName</span></span>
<span data-ttu-id="1ffe7-112">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="1ffe7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffe7-113">-DefaultProfile</span></span>
<span data-ttu-id="1ffe7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffe7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffe7-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ffe7-116">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1ffe7-117">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1ffe7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ffe7-118">-SubscriptionId</span></span>
<span data-ttu-id="1ffe7-119">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ffe7-120">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ffe7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ffe7-121">-Confirm</span></span>
<span data-ttu-id="1ffe7-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ffe7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffe7-123">-WhatIf</span></span>
<span data-ttu-id="1ffe7-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1ffe7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ffe7-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ffe7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffe7-126">CommonParameters</span></span>
<span data-ttu-id="1ffe7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffe7-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ffe7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffe7-129">입력</span><span class="sxs-lookup"><span data-stu-id="1ffe7-129">INPUTS</span></span>

## <span data-ttu-id="1ffe7-130">출력</span><span class="sxs-lookup"><span data-stu-id="1ffe7-130">OUTPUTS</span></span>

### <span data-ttu-id="1ffe7-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1ffe7-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="1ffe7-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ffe7-132">NOTES</span></span>

<span data-ttu-id="1ffe7-133">별칭</span><span class="sxs-lookup"><span data-stu-id="1ffe7-133">ALIASES</span></span>

## <span data-ttu-id="1ffe7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ffe7-134">RELATED LINKS</span></span>

