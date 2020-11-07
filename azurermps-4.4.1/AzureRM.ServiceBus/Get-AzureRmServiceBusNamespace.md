---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702194"
---
# <span data-ttu-id="61958-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="61958-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="61958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61958-102">SYNOPSIS</span></span>
<span data-ttu-id="61958-103">리소스 그룹 내에서 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="61958-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61958-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61958-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61958-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61958-105">DESCRIPTION</span></span>
<span data-ttu-id="61958-106">**AzureRmServiceBusNamespace** cmdlet은 리소스 그룹 내의 지정 된 Service Bus 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="61958-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="61958-107">예제의</span><span class="sxs-lookup"><span data-stu-id="61958-107">EXAMPLES</span></span>

### <span data-ttu-id="61958-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="61958-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="61958-109">지정 된 Service Bus 네임 스페이스에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="61958-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="61958-110">변수</span><span class="sxs-lookup"><span data-stu-id="61958-110">PARAMETERS</span></span>

### <span data-ttu-id="61958-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61958-111">-DefaultProfile</span></span>
<span data-ttu-id="61958-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61958-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61958-113">-이름</span><span class="sxs-lookup"><span data-stu-id="61958-113">-Name</span></span>
<span data-ttu-id="61958-114">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61958-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61958-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61958-115">-ResourceGroupName</span></span>
<span data-ttu-id="61958-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61958-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61958-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61958-117">CommonParameters</span></span>
<span data-ttu-id="61958-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61958-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61958-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61958-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61958-120">입력</span><span class="sxs-lookup"><span data-stu-id="61958-120">INPUTS</span></span>

### <span data-ttu-id="61958-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61958-121">-ResourceGroup</span></span>
<span data-ttu-id="61958-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61958-122">System.String</span></span>

### <span data-ttu-id="61958-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="61958-123">-NamespaceName</span></span>
 <span data-ttu-id="61958-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61958-124">System.String</span></span>

## <span data-ttu-id="61958-125">출력</span><span class="sxs-lookup"><span data-stu-id="61958-125">OUTPUTS</span></span>

### <span data-ttu-id="61958-126">ServiceBus ' 1 [[Microsoft Azure. NamespaceAttributes, Microsoft Azure. ServiceBus, Version = 0.0.1.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="61958-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="61958-127">이름: SB-Example1 Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 위치: 서쪽 미국 Sku: 이름: 표준, 용량: 1, 계층: 표준 ProvisioningState: 성공 상태: 활성 CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ 활성화 됨: True</span><span class="sxs-lookup"><span data-stu-id="61958-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="61958-128">상속자</span><span class="sxs-lookup"><span data-stu-id="61958-128">NOTES</span></span>
## <span data-ttu-id="61958-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61958-129">RELATED LINKS</span></span>

## <span data-ttu-id="61958-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61958-130">RELATED LINKS</span></span>

