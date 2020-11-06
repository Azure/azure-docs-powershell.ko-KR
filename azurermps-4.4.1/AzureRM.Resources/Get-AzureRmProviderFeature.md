---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533007"
---
# <span data-ttu-id="c6810-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c6810-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c6810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6810-102">SYNOPSIS</span></span>
<span data-ttu-id="c6810-103">Azure 공급자 기능에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6810-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6810-104">SYNTAX</span></span>

### <span data-ttu-id="c6810-105">ListAvailableParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6810-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6810-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="c6810-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6810-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c6810-107">DESCRIPTION</span></span>
<span data-ttu-id="c6810-108">**AzureRmProviderFeature** cmdlet은 기능 이름, 공급자 이름 및 Azure 공급자 기능에 대 한 등록 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="c6810-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c6810-109">EXAMPLES</span></span>

### <span data-ttu-id="c6810-110">예제 1: 사용할 수 있는 모든 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6810-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="c6810-111">이 명령은 사용할 수 있는 모든 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-111">This command gets all available features.</span></span>

### <span data-ttu-id="c6810-112">예제 2: 특정 기능에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6810-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="c6810-113">이 명령은 지정 된 공급자에 대 한 AllowPreReleaseRegions 이라는 기능에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="c6810-114">변수</span><span class="sxs-lookup"><span data-stu-id="c6810-114">PARAMETERS</span></span>

### <span data-ttu-id="c6810-115">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="c6810-115">-FeatureName</span></span>
<span data-ttu-id="c6810-116">가져올 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-116">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6810-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c6810-117">-ListAvailable</span></span>
<span data-ttu-id="c6810-118">이 cmdlet에 모든 기능이 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-118">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6810-119">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c6810-119">-ProviderNamespace</span></span>
<span data-ttu-id="c6810-120">이 cmdlet이 공급자 기능을 가져오는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6810-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6810-121">-DefaultProfile</span></span>
<span data-ttu-id="c6810-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6810-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6810-123">CommonParameters</span></span>
<span data-ttu-id="c6810-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6810-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6810-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6810-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6810-126">입력</span><span class="sxs-lookup"><span data-stu-id="c6810-126">INPUTS</span></span>

## <span data-ttu-id="c6810-127">출력</span><span class="sxs-lookup"><span data-stu-id="c6810-127">OUTPUTS</span></span>

### <span data-ttu-id="c6810-128">System.webserver. List ' 1 [SdkModels. t e m. m m Providerfeature]</span><span class="sxs-lookup"><span data-stu-id="c6810-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="c6810-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c6810-129">NOTES</span></span>

## <span data-ttu-id="c6810-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6810-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6810-131">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c6810-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


