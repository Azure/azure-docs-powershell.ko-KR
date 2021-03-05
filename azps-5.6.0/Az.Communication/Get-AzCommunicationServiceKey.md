---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991648"
---
# <span data-ttu-id="b6951-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="b6951-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="b6951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6951-102">SYNOPSIS</span></span>
<span data-ttu-id="b6951-103">CommunicationService 리소스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="b6951-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6951-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6951-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6951-105">DESCRIPTION</span></span>
<span data-ttu-id="b6951-106">CommunicationService 리소스의 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="b6951-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6951-107">EXAMPLES</span></span>

### <span data-ttu-id="b6951-108">예제 1: 지정된 Communcation 서비스에 대한 키를 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="b6951-109">지정된 통신 서비스에 대한 ConnectionString 및 키를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="b6951-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6951-110">PARAMETERS</span></span>

### <span data-ttu-id="b6951-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="b6951-111">-CommunicationServiceName</span></span>
<span data-ttu-id="b6951-112">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="b6951-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6951-113">-DefaultProfile</span></span>
<span data-ttu-id="b6951-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6951-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6951-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6951-116">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b6951-117">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b6951-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6951-118">-SubscriptionId</span></span>
<span data-ttu-id="b6951-119">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b6951-120">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6951-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b6951-121">-Confirm</span></span>
<span data-ttu-id="b6951-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6951-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6951-123">-WhatIf</span></span>
<span data-ttu-id="b6951-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6951-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6951-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6951-126">CommonParameters</span></span>
<span data-ttu-id="b6951-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6951-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6951-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6951-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6951-129">입력</span><span class="sxs-lookup"><span data-stu-id="b6951-129">INPUTS</span></span>

## <span data-ttu-id="b6951-130">출력</span><span class="sxs-lookup"><span data-stu-id="b6951-130">OUTPUTS</span></span>

### <span data-ttu-id="b6951-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b6951-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="b6951-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6951-132">NOTES</span></span>

<span data-ttu-id="b6951-133">별칭</span><span class="sxs-lookup"><span data-stu-id="b6951-133">ALIASES</span></span>

## <span data-ttu-id="b6951-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6951-134">RELATED LINKS</span></span>

