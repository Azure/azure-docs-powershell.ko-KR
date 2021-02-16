---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186481"
---
# <span data-ttu-id="48cf2-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="48cf2-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="48cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="48cf2-103">Azure 공급자 기능에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="48cf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="48cf2-104">SYNTAX</span></span>

### <span data-ttu-id="48cf2-105">ListAvailableParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="48cf2-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48cf2-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="48cf2-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48cf2-107">설명</span><span class="sxs-lookup"><span data-stu-id="48cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="48cf2-108">**Get-AzProviderFeature** cmdlet은 Azure 공급자 기능에 대한 기능 이름, 공급자 이름 및 등록 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="48cf2-109">예제</span><span class="sxs-lookup"><span data-stu-id="48cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="48cf2-110">예제 1: 사용 가능한 모든 기능 다운로드</span><span class="sxs-lookup"><span data-stu-id="48cf2-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="48cf2-111">이 명령은 사용 가능한 모든 기능을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-111">This command gets all available features.</span></span>

### <span data-ttu-id="48cf2-112">예제 2: 특정 기능에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="48cf2-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="48cf2-113">이 명령은 지정된 공급자에 대한 AllowPreReleaseRegions라는 기능에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="48cf2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="48cf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cf2-115">-DefaultProfile</span></span>
<span data-ttu-id="48cf2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48cf2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48cf2-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="48cf2-117">-FeatureName</span></span>
<span data-ttu-id="48cf2-118">얻을 기능의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="48cf2-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="48cf2-119">-ListAvailable</span></span>
<span data-ttu-id="48cf2-120">이 cmdlet이 모든 기능을 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="48cf2-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="48cf2-121">-ProviderNamespace</span></span>
<span data-ttu-id="48cf2-122">이 cmdlet에서 공급자 기능을 얻을 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="48cf2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cf2-123">CommonParameters</span></span>
<span data-ttu-id="48cf2-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48cf2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cf2-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48cf2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cf2-126">입력</span><span class="sxs-lookup"><span data-stu-id="48cf2-126">INPUTS</span></span>

### <span data-ttu-id="48cf2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="48cf2-127">System.String</span></span>

## <span data-ttu-id="48cf2-128">출력</span><span class="sxs-lookup"><span data-stu-id="48cf2-128">OUTPUTS</span></span>

### <span data-ttu-id="48cf2-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="48cf2-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="48cf2-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48cf2-130">NOTES</span></span>

## <span data-ttu-id="48cf2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48cf2-131">RELATED LINKS</span></span>

[<span data-ttu-id="48cf2-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="48cf2-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


