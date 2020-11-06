---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 468128f16c3a5ef7ef4b400694dbcc1c570f5488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537516"
---
# <span data-ttu-id="4bc6b-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="4bc6b-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="4bc6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc6b-103">릴레이 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bc6b-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bc6b-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc6b-106">**AzureRmRelayHybridConnection** Cmdlet은 Relay 네임 스페이스 내에서 지정 된 HybridConnection에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="4bc6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4bc6b-107">EXAMPLES</span></span>

### <span data-ttu-id="4bc6b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bc6b-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="4bc6b-109">HybridConnection의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="4bc6b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4bc6b-110">PARAMETERS</span></span>

### <span data-ttu-id="4bc6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc6b-111">-DefaultProfile</span></span>
<span data-ttu-id="4bc6b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc6b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4bc6b-113">-Name</span></span>
<span data-ttu-id="4bc6b-114">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="4bc6b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4bc6b-115">-Namespace</span></span>
<span data-ttu-id="4bc6b-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4bc6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4bc6b-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4bc6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc6b-119">CommonParameters</span></span>
<span data-ttu-id="4bc6b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4bc6b-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc6b-122">입력</span><span class="sxs-lookup"><span data-stu-id="4bc6b-122">INPUTS</span></span>

### <span data-ttu-id="4bc6b-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bc6b-123">System.String</span></span>


## <span data-ttu-id="4bc6b-124">출력</span><span class="sxs-lookup"><span data-stu-id="4bc6b-124">OUTPUTS</span></span>

### <span data-ttu-id="4bc6b-125">PSHybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="4bc6b-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="4bc6b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4bc6b-126">NOTES</span></span>

## <span data-ttu-id="4bc6b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bc6b-127">RELATED LINKS</span></span>
