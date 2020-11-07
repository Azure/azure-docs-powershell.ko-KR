---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 86cffb4016423d9d998127ad3ee26f9644941f05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711412"
---
# <span data-ttu-id="a7544-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="a7544-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="a7544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7544-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7544-103">구문과</span><span class="sxs-lookup"><span data-stu-id="a7544-103">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7544-104">설명은</span><span class="sxs-lookup"><span data-stu-id="a7544-104">DESCRIPTION</span></span>

## <span data-ttu-id="a7544-105">예제의</span><span class="sxs-lookup"><span data-stu-id="a7544-105">EXAMPLES</span></span>

## <span data-ttu-id="a7544-106">변수</span><span class="sxs-lookup"><span data-stu-id="a7544-106">PARAMETERS</span></span>

### <span data-ttu-id="a7544-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7544-107">-DefaultProfile</span></span>
<span data-ttu-id="a7544-108">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7544-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7544-109">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a7544-109">-DomainNameLabel</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7544-110">-위치</span><span class="sxs-lookup"><span data-stu-id="a7544-110">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7544-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7544-111">CommonParameters</span></span>
<span data-ttu-id="a7544-112">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7544-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7544-113">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7544-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7544-114">입력</span><span class="sxs-lookup"><span data-stu-id="a7544-114">INPUTS</span></span>

### <span data-ttu-id="a7544-115">않아야</span><span class="sxs-lookup"><span data-stu-id="a7544-115">None</span></span>
<span data-ttu-id="a7544-116">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7544-116">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7544-117">출력</span><span class="sxs-lookup"><span data-stu-id="a7544-117">OUTPUTS</span></span>

### <span data-ttu-id="a7544-118">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a7544-118">System.Boolean</span></span>

## <span data-ttu-id="a7544-119">상속자</span><span class="sxs-lookup"><span data-stu-id="a7544-119">NOTES</span></span>

## <span data-ttu-id="a7544-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7544-120">RELATED LINKS</span></span>

