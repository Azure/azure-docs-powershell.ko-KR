---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
ms.openlocfilehash: c5d9d2131ff144f04794d2cf283aaf51ed1450e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881766"
---
# <span data-ttu-id="179e0-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="179e0-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="179e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179e0-102">SYNOPSIS</span></span>
<span data-ttu-id="179e0-103">각 위치에 대해 지원 되는 리소스 공급자 및 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="179e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="179e0-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="179e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="179e0-105">DESCRIPTION</span></span>
<span data-ttu-id="179e0-106">**AzureRmLocation** cmdlet은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="179e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="179e0-107">EXAMPLES</span></span>

### <span data-ttu-id="179e0-108">예제 1: 모든 위치 및 지원 되는 리소스 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="179e0-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="179e0-109">이 명령은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="179e0-110">변수</span><span class="sxs-lookup"><span data-stu-id="179e0-110">PARAMETERS</span></span>

### <span data-ttu-id="179e0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="179e0-111">-ApiVersion</span></span>
<span data-ttu-id="179e0-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="179e0-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179e0-114">-DefaultProfile</span></span>
<span data-ttu-id="179e0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="179e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="179e0-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="179e0-116">-Pre</span></span>
<span data-ttu-id="179e0-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179e0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179e0-118">CommonParameters</span></span>
<span data-ttu-id="179e0-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="179e0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179e0-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179e0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179e0-121">입력</span><span class="sxs-lookup"><span data-stu-id="179e0-121">INPUTS</span></span>

## <span data-ttu-id="179e0-122">출력</span><span class="sxs-lookup"><span data-stu-id="179e0-122">OUTPUTS</span></span>

## <span data-ttu-id="179e0-123">상속자</span><span class="sxs-lookup"><span data-stu-id="179e0-123">NOTES</span></span>

## <span data-ttu-id="179e0-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="179e0-124">RELATED LINKS</span></span>