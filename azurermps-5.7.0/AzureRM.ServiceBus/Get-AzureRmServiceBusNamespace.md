---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528804"
---
# <span data-ttu-id="2afd6-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="2afd6-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="2afd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2afd6-102">SYNOPSIS</span></span>
<span data-ttu-id="2afd6-103">리소스 그룹 내에서 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2afd6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2afd6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2afd6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2afd6-105">DESCRIPTION</span></span>
<span data-ttu-id="2afd6-106">**AzureRmServiceBusNamespace** cmdlet은 리소스 그룹 내의 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="2afd6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2afd6-107">EXAMPLES</span></span>

### <span data-ttu-id="2afd6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2afd6-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="2afd6-109">변수</span><span class="sxs-lookup"><span data-stu-id="2afd6-109">PARAMETERS</span></span>

### <span data-ttu-id="2afd6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afd6-110">-DefaultProfile</span></span>
<span data-ttu-id="2afd6-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2afd6-112">-이름</span><span class="sxs-lookup"><span data-stu-id="2afd6-112">-Name</span></span>
<span data-ttu-id="2afd6-113">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afd6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2afd6-114">-ResourceGroupName</span></span>
<span data-ttu-id="2afd6-115">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afd6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afd6-116">CommonParameters</span></span>
<span data-ttu-id="2afd6-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afd6-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afd6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afd6-119">입력</span><span class="sxs-lookup"><span data-stu-id="2afd6-119">INPUTS</span></span>

### <span data-ttu-id="2afd6-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2afd6-120">-ResourceGroup</span></span>
<span data-ttu-id="2afd6-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2afd6-121">System.String</span></span>

### <span data-ttu-id="2afd6-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2afd6-122">-NamespaceName</span></span>
 <span data-ttu-id="2afd6-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2afd6-123">System.String</span></span>

## <span data-ttu-id="2afd6-124">출력</span><span class="sxs-lookup"><span data-stu-id="2afd6-124">OUTPUTS</span></span>

### <span data-ttu-id="2afd6-125">ServiceBus ' 1 [[Microsoft Azure. PSNamespaceAttributes, Microsoft Azure. ServiceBus, Version = 0.0.1.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2afd6-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2afd6-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2afd6-126">NOTES</span></span>

## <span data-ttu-id="2afd6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2afd6-127">RELATED LINKS</span></span>

