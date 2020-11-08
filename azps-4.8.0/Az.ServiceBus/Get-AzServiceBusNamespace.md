---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047625"
---
# <span data-ttu-id="ab073-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ab073-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="ab073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab073-102">SYNOPSIS</span></span>
<span data-ttu-id="ab073-103">리소스 그룹 내에서 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ab073-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab073-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab073-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab073-105">DESCRIPTION</span></span>
<span data-ttu-id="ab073-106">**AzServiceBusNamespace** cmdlet은 리소스 그룹 내의 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ab073-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab073-107">EXAMPLES</span></span>

### <span data-ttu-id="ab073-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab073-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="ab073-109">변수</span><span class="sxs-lookup"><span data-stu-id="ab073-109">PARAMETERS</span></span>

### <span data-ttu-id="ab073-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab073-110">-DefaultProfile</span></span>
<span data-ttu-id="ab073-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab073-112">-이름</span><span class="sxs-lookup"><span data-stu-id="ab073-112">-Name</span></span>
<span data-ttu-id="ab073-113">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab073-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab073-114">-ResourceGroupName</span></span>
<span data-ttu-id="ab073-115">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab073-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab073-116">CommonParameters</span></span>
<span data-ttu-id="ab073-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab073-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab073-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab073-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab073-119">입력</span><span class="sxs-lookup"><span data-stu-id="ab073-119">INPUTS</span></span>

### <span data-ttu-id="ab073-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab073-120">System.String</span></span>

## <span data-ttu-id="ab073-121">출력</span><span class="sxs-lookup"><span data-stu-id="ab073-121">OUTPUTS</span></span>

### <span data-ttu-id="ab073-122">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="ab073-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ab073-123">상속자</span><span class="sxs-lookup"><span data-stu-id="ab073-123">NOTES</span></span>

## <span data-ttu-id="ab073-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab073-124">RELATED LINKS</span></span>
