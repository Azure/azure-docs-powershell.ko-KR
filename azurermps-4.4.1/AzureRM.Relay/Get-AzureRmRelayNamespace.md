---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529180"
---
# <span data-ttu-id="84e9a-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="84e9a-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="84e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="84e9a-103">리소스 그룹 내에서 지정 된 릴레이 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84e9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84e9a-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="84e9a-106">**AzureRmRelayNamespace** cmdlet은 리소스 그룹 내의 지정 된 릴레이 네임 스페이스에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="84e9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="84e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="84e9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="84e9a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="84e9a-109">지정 된 릴레이 네임 스페이스에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="84e9a-110">변수</span><span class="sxs-lookup"><span data-stu-id="84e9a-110">PARAMETERS</span></span>

### <span data-ttu-id="84e9a-111">-이름</span><span class="sxs-lookup"><span data-stu-id="84e9a-111">-Name</span></span>
<span data-ttu-id="84e9a-112">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-112">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e9a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e9a-113">-ResourceGroupName</span></span>
<span data-ttu-id="84e9a-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e9a-115">-DefaultProfile</span></span>
<span data-ttu-id="84e9a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e9a-117">CommonParameters</span></span>
<span data-ttu-id="84e9a-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e9a-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e9a-120">입력</span><span class="sxs-lookup"><span data-stu-id="84e9a-120">INPUTS</span></span>

### <span data-ttu-id="84e9a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e9a-121">-ResourceGroupName</span></span>
<span data-ttu-id="84e9a-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84e9a-122">System.String</span></span>

### <span data-ttu-id="84e9a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="84e9a-123">-Name</span></span>
 <span data-ttu-id="84e9a-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84e9a-124">System.String</span></span>

## <span data-ttu-id="84e9a-125">출력</span><span class="sxs-lookup"><span data-stu-id="84e9a-125">OUTPUTS</span></span>

### <span data-ttu-id="84e9a-126">System.webserver. List ' 1 [[RelayNamespaceAttributes, Microsoft azure. 0.1.0.0, system.webserver, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="84e9a-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="84e9a-127">ProvisioningState: 성공 CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-Relay1 Location: 서쪽 US 태그: {[tag1, Tag1Value]} Id:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 이름: TestNameSpace-Relay1 종류: Microsoft. 릴레이/네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="84e9a-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="84e9a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="84e9a-128">NOTES</span></span>

## <span data-ttu-id="84e9a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84e9a-129">RELATED LINKS</span></span>

