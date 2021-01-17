---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490347"
---
# <span data-ttu-id="60aed-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="60aed-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="60aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aed-102">SYNOPSIS</span></span>
<span data-ttu-id="60aed-103">계정에 Azure 공급자 기능을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="60aed-104">구문</span><span class="sxs-lookup"><span data-stu-id="60aed-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60aed-105">설명</span><span class="sxs-lookup"><span data-stu-id="60aed-105">DESCRIPTION</span></span>
<span data-ttu-id="60aed-106">**Register-AzProviderFeature** cmdlet은 계정에 Azure 공급자 기능을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="60aed-107">예제</span><span class="sxs-lookup"><span data-stu-id="60aed-107">EXAMPLES</span></span>

### <span data-ttu-id="60aed-108">예제 1: 기능 등록</span><span class="sxs-lookup"><span data-stu-id="60aed-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="60aed-109">그러면 Microsoft.Network에 대한 AllowApplicationSecurityGroups 기능이 계정에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="60aed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60aed-110">PARAMETERS</span></span>

### <span data-ttu-id="60aed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aed-111">-DefaultProfile</span></span>
<span data-ttu-id="60aed-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60aed-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60aed-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="60aed-113">-FeatureName</span></span>
<span data-ttu-id="60aed-114">이 cmdlet이 등록하는 기능의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aed-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="60aed-115">-ProviderNamespace</span></span>
<span data-ttu-id="60aed-116">이 cmdlet이 공급자 기능을 등록하는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aed-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60aed-117">-Confirm</span></span>
<span data-ttu-id="60aed-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60aed-119">-WhatIf</span></span>
<span data-ttu-id="60aed-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="60aed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60aed-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aed-122">CommonParameters</span></span>
<span data-ttu-id="60aed-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60aed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aed-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60aed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aed-125">입력</span><span class="sxs-lookup"><span data-stu-id="60aed-125">INPUTS</span></span>

### <span data-ttu-id="60aed-126">System.String</span><span class="sxs-lookup"><span data-stu-id="60aed-126">System.String</span></span>

## <span data-ttu-id="60aed-127">출력</span><span class="sxs-lookup"><span data-stu-id="60aed-127">OUTPUTS</span></span>

### <span data-ttu-id="60aed-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="60aed-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="60aed-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60aed-129">NOTES</span></span>

## <span data-ttu-id="60aed-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60aed-130">RELATED LINKS</span></span>

[<span data-ttu-id="60aed-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="60aed-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


