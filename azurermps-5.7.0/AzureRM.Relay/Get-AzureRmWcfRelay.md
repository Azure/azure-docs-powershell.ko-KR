---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534732"
---
# <span data-ttu-id="7341a-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="7341a-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="7341a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7341a-102">SYNOPSIS</span></span>
<span data-ttu-id="7341a-103">지정 된 WcfRelay에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7341a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7341a-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7341a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7341a-105">DESCRIPTION</span></span>
<span data-ttu-id="7341a-106">**AzureRmWcfRelay** cmdlet은 지정 된 WcfRelay에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="7341a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7341a-107">EXAMPLES</span></span>

### <span data-ttu-id="7341a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7341a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="7341a-109">WcfRelay의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="7341a-110">변수</span><span class="sxs-lookup"><span data-stu-id="7341a-110">PARAMETERS</span></span>

### <span data-ttu-id="7341a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7341a-111">-DefaultProfile</span></span>
<span data-ttu-id="7341a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7341a-113">-이름</span><span class="sxs-lookup"><span data-stu-id="7341a-113">-Name</span></span>
<span data-ttu-id="7341a-114">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7341a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7341a-115">-Namespace</span></span>
<span data-ttu-id="7341a-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7341a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7341a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7341a-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7341a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7341a-119">CommonParameters</span></span>
<span data-ttu-id="7341a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7341a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7341a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7341a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7341a-122">입력</span><span class="sxs-lookup"><span data-stu-id="7341a-122">INPUTS</span></span>

### <span data-ttu-id="7341a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7341a-123">-ResourceGroupName</span></span>
 <span data-ttu-id="7341a-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7341a-124">System.String</span></span>
 

### <span data-ttu-id="7341a-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7341a-125">-Namespace</span></span>
 <span data-ttu-id="7341a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7341a-126">System.String</span></span>
 

### <span data-ttu-id="7341a-127">-이름</span><span class="sxs-lookup"><span data-stu-id="7341a-127">-Name</span></span>
 <span data-ttu-id="7341a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7341a-128">System.String</span></span> 

## <span data-ttu-id="7341a-129">출력</span><span class="sxs-lookup"><span data-stu-id="7341a-129">OUTPUTS</span></span>

### <span data-ttu-id="7341a-130">System.webserver. List ' 1 [[WcfRelayAttributes, Microsoft azure. 0.1.0.0, system.webserver, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7341a-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="7341a-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: True로 설정 됨 RequiresTransportSecurity: true IsDynamic: False UserMetadata: 사용자 메타 데이터 Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name: TestWCFRelay1 Type: Microsoft. 릴레이/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="7341a-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="7341a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7341a-132">NOTES</span></span>

## <span data-ttu-id="7341a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7341a-133">RELATED LINKS</span></span>

