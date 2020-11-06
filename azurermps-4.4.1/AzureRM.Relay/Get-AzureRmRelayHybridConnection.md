---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529181"
---
# <span data-ttu-id="3b9cb-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="3b9cb-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="3b9cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9cb-103">릴레이 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b9cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b9cb-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b9cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b9cb-105">DESCRIPTION</span></span>
<span data-ttu-id="3b9cb-106">**AzureRmRelayHybridConnection** Cmdlet은 Relay 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3b9cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b9cb-107">EXAMPLES</span></span>

### <span data-ttu-id="3b9cb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3b9cb-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="3b9cb-109">HybridConnection의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="3b9cb-110">변수</span><span class="sxs-lookup"><span data-stu-id="3b9cb-110">PARAMETERS</span></span>

### <span data-ttu-id="3b9cb-111">-이름</span><span class="sxs-lookup"><span data-stu-id="3b9cb-111">-Name</span></span>
<span data-ttu-id="3b9cb-112">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-112">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9cb-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b9cb-113">-Namespace</span></span>
<span data-ttu-id="3b9cb-114">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="3b9cb-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9cb-117">-DefaultProfile</span></span>
<span data-ttu-id="3b9cb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b9cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9cb-119">CommonParameters</span></span>
<span data-ttu-id="3b9cb-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b9cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9cb-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9cb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9cb-122">입력</span><span class="sxs-lookup"><span data-stu-id="3b9cb-122">INPUTS</span></span>

### <span data-ttu-id="3b9cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9cb-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="3b9cb-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b9cb-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="3b9cb-125">-이름</span><span class="sxs-lookup"><span data-stu-id="3b9cb-125">-Name</span></span>
    System.String

## <span data-ttu-id="3b9cb-126">출력</span><span class="sxs-lookup"><span data-stu-id="3b9cb-126">OUTPUTS</span></span>

### <span data-ttu-id="3b9cb-127">System.webserver. List ' 1 [[HybridConnectionAttibutes, Microsoft azure. 0.1.0.0, system.webserver, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3b9cb-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3b9cb-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: True UserMetadata: 사용자 메타 데이터 Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="3b9cb-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="3b9cb-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3b9cb-129">NOTES</span></span>

## <span data-ttu-id="3b9cb-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b9cb-130">RELATED LINKS</span></span>

