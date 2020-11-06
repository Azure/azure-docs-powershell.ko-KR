---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528823"
---
# <span data-ttu-id="31cac-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="31cac-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="31cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31cac-102">SYNOPSIS</span></span>
<span data-ttu-id="31cac-103">계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31cac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31cac-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31cac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31cac-105">DESCRIPTION</span></span>
<span data-ttu-id="31cac-106">**AzureRmProviderFeature** cmdlet은 계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="31cac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31cac-107">EXAMPLES</span></span>

### <span data-ttu-id="31cac-108">예제 1: 기능 등록</span><span class="sxs-lookup"><span data-stu-id="31cac-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="31cac-109">이렇게 하면 Microsoft. 네트워크에 대 한 AllowApplicationSecurityGroups 기능이 계정에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="31cac-110">변수</span><span class="sxs-lookup"><span data-stu-id="31cac-110">PARAMETERS</span></span>

### <span data-ttu-id="31cac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cac-111">-DefaultProfile</span></span>
<span data-ttu-id="31cac-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31cac-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31cac-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="31cac-113">-FeatureName</span></span>
<span data-ttu-id="31cac-114">이 cmdlet이 등록 하는 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cac-115">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="31cac-115">-ProviderNamespace</span></span>
<span data-ttu-id="31cac-116">이 cmdlet이 공급자 기능을 등록할 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31cac-117">-확인</span><span class="sxs-lookup"><span data-stu-id="31cac-117">-Confirm</span></span>
<span data-ttu-id="31cac-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31cac-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31cac-119">-WhatIf</span></span>
<span data-ttu-id="31cac-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31cac-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31cac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cac-122">CommonParameters</span></span>
<span data-ttu-id="31cac-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cac-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31cac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cac-125">입력</span><span class="sxs-lookup"><span data-stu-id="31cac-125">INPUTS</span></span>

### <span data-ttu-id="31cac-126">않아야</span><span class="sxs-lookup"><span data-stu-id="31cac-126">None</span></span>
<span data-ttu-id="31cac-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31cac-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31cac-128">출력</span><span class="sxs-lookup"><span data-stu-id="31cac-128">OUTPUTS</span></span>

### <span data-ttu-id="31cac-129">System.webserver. List ' 1 [SdkModels. t e m. m m Providerfeature]</span><span class="sxs-lookup"><span data-stu-id="31cac-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="31cac-130">상속자</span><span class="sxs-lookup"><span data-stu-id="31cac-130">NOTES</span></span>

## <span data-ttu-id="31cac-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31cac-131">RELATED LINKS</span></span>

[<span data-ttu-id="31cac-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="31cac-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


