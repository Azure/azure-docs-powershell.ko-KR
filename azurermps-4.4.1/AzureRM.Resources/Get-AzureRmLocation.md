---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536192"
---
# <span data-ttu-id="e3b75-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="e3b75-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="e3b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b75-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b75-103">각 위치에 대해 지원 되는 리소스 공급자 및 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3b75-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3b75-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b75-106">**AzureRmLocation** cmdlet은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e3b75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3b75-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b75-108">예제 1: 모든 위치 및 지원 되는 리소스 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3b75-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="e3b75-109">이 명령은 각 위치에 대해 지원 되는 리소스 공급자와 모든 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e3b75-110">변수</span><span class="sxs-lookup"><span data-stu-id="e3b75-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b75-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e3b75-111">-ApiVersion</span></span>
<span data-ttu-id="e3b75-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e3b75-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e3b75-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="e3b75-114">-Pre</span></span>
<span data-ttu-id="e3b75-115">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e3b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b75-116">-DefaultProfile</span></span>
<span data-ttu-id="e3b75-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b75-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b75-118">CommonParameters</span></span>
<span data-ttu-id="e3b75-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b75-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b75-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b75-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b75-121">입력</span><span class="sxs-lookup"><span data-stu-id="e3b75-121">INPUTS</span></span>

## <span data-ttu-id="e3b75-122">출력</span><span class="sxs-lookup"><span data-stu-id="e3b75-122">OUTPUTS</span></span>

### <span data-ttu-id="e3b75-123">System.webserver. List ' 1 [Microsoft SdkModels. t e m. m a n.</span><span class="sxs-lookup"><span data-stu-id="e3b75-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="e3b75-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e3b75-124">NOTES</span></span>

## <span data-ttu-id="e3b75-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3b75-125">RELATED LINKS</span></span>

