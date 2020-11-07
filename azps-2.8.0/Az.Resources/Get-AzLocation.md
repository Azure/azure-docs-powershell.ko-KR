---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 17bc16b38bc967f9997b22d7dd86b056253d8a18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873402"
---
# <span data-ttu-id="7c32b-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="7c32b-101">Get-AzLocation</span></span>

## <span data-ttu-id="7c32b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c32b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c32b-103">각 위치에 대해 지원 되는 리소스 공급자 및 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7c32b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c32b-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c32b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c32b-105">DESCRIPTION</span></span>
<span data-ttu-id="7c32b-106">**AzLocation** cmdlet은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7c32b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c32b-107">EXAMPLES</span></span>

### <span data-ttu-id="7c32b-108">예제 1: 모든 위치 및 지원 되는 리소스 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c32b-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="7c32b-109">이 명령은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7c32b-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c32b-110">PARAMETERS</span></span>

### <span data-ttu-id="7c32b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c32b-111">-ApiVersion</span></span>
<span data-ttu-id="7c32b-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7c32b-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7c32b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c32b-114">-DefaultProfile</span></span>
<span data-ttu-id="7c32b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c32b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c32b-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c32b-116">-Pre</span></span>
<span data-ttu-id="7c32b-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c32b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c32b-118">CommonParameters</span></span>
<span data-ttu-id="7c32b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c32b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c32b-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c32b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c32b-121">입력</span><span class="sxs-lookup"><span data-stu-id="7c32b-121">INPUTS</span></span>

### <span data-ttu-id="7c32b-122">않아야</span><span class="sxs-lookup"><span data-stu-id="7c32b-122">None</span></span>

## <span data-ttu-id="7c32b-123">출력</span><span class="sxs-lookup"><span data-stu-id="7c32b-123">OUTPUTS</span></span>

### <span data-ttu-id="7c32b-124">SdkModels to PSResourceProviderLocation (.</span><span class="sxs-lookup"><span data-stu-id="7c32b-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="7c32b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="7c32b-125">NOTES</span></span>

## <span data-ttu-id="7c32b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c32b-126">RELATED LINKS</span></span>
