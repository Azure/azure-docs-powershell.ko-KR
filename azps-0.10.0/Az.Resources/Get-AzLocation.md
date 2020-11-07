---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 4aedbb502780a08d0ce5556af84a445ab44552f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876490"
---
# <span data-ttu-id="bc9ba-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="bc9ba-101">Get-AzLocation</span></span>

## <span data-ttu-id="bc9ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9ba-103">각 위치에 대해 지원 되는 리소스 공급자 및 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bc9ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc9ba-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc9ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9ba-106">**AzLocation** cmdlet은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bc9ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc9ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bc9ba-108">예제 1: 모든 위치 및 지원 되는 리소스 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc9ba-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="bc9ba-109">이 명령은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bc9ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="bc9ba-110">PARAMETERS</span></span>

### <span data-ttu-id="bc9ba-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc9ba-111">-ApiVersion</span></span>
<span data-ttu-id="bc9ba-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="bc9ba-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="bc9ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9ba-114">-DefaultProfile</span></span>
<span data-ttu-id="bc9ba-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bc9ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9ba-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="bc9ba-116">-Pre</span></span>
<span data-ttu-id="bc9ba-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bc9ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9ba-118">CommonParameters</span></span>
<span data-ttu-id="bc9ba-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc9ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9ba-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc9ba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9ba-121">입력</span><span class="sxs-lookup"><span data-stu-id="bc9ba-121">INPUTS</span></span>

## <span data-ttu-id="bc9ba-122">출력</span><span class="sxs-lookup"><span data-stu-id="bc9ba-122">OUTPUTS</span></span>

## <span data-ttu-id="bc9ba-123">상속자</span><span class="sxs-lookup"><span data-stu-id="bc9ba-123">NOTES</span></span>

## <span data-ttu-id="bc9ba-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc9ba-124">RELATED LINKS</span></span>
