---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490560"
---
# <span data-ttu-id="e9e94-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="e9e94-101">Get-AzLocation</span></span>

## <span data-ttu-id="e9e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e94-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e94-103">각 위치에 대해 모든 위치 및 지원되는 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e9e94-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9e94-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e94-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9e94-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e94-106">**Get-AzLocation** cmdlet은 각 위치에 대해 모든 위치 및 지원되는 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e9e94-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9e94-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e94-108">예제 1: 모든 위치 및 지원되는 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="e9e94-109">이 명령은 각 위치에 대해 모든 위치 및 지원되는 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e9e94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e94-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e94-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e9e94-111">-ApiVersion</span></span>
<span data-ttu-id="e9e94-112">리소스 공급자가 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e9e94-113">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e9e94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e94-114">-DefaultProfile</span></span>
<span data-ttu-id="e9e94-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9e94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9e94-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e9e94-116">-Pre</span></span>
<span data-ttu-id="e9e94-117">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e9e94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e94-118">CommonParameters</span></span>
<span data-ttu-id="e9e94-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e94-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9e94-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e94-121">입력</span><span class="sxs-lookup"><span data-stu-id="e9e94-121">INPUTS</span></span>

### <span data-ttu-id="e9e94-122">없음</span><span class="sxs-lookup"><span data-stu-id="e9e94-122">None</span></span>

## <span data-ttu-id="e9e94-123">출력</span><span class="sxs-lookup"><span data-stu-id="e9e94-123">OUTPUTS</span></span>

### <span data-ttu-id="e9e94-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="e9e94-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="e9e94-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9e94-125">NOTES</span></span>

## <span data-ttu-id="e9e94-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9e94-126">RELATED LINKS</span></span>
