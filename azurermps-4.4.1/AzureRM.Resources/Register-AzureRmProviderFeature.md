---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532964"
---
# <span data-ttu-id="19a8a-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="19a8a-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="19a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="19a8a-103">계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19a8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19a8a-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19a8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="19a8a-106">**AzureRmProviderFeature** cmdlet은 계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="19a8a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19a8a-107">EXAMPLES</span></span>

## <span data-ttu-id="19a8a-108">변수</span><span class="sxs-lookup"><span data-stu-id="19a8a-108">PARAMETERS</span></span>

### <span data-ttu-id="19a8a-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="19a8a-109">-FeatureName</span></span>
<span data-ttu-id="19a8a-110">이 cmdlet이 등록 하는 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="19a8a-111">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="19a8a-111">-ProviderNamespace</span></span>
<span data-ttu-id="19a8a-112">이 cmdlet이 공급자 기능을 등록할 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="19a8a-113">-확인</span><span class="sxs-lookup"><span data-stu-id="19a8a-113">-Confirm</span></span>
<span data-ttu-id="19a8a-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19a8a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19a8a-115">-WhatIf</span></span>
<span data-ttu-id="19a8a-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19a8a-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19a8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a8a-118">-DefaultProfile</span></span>
<span data-ttu-id="19a8a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19a8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a8a-120">CommonParameters</span></span>
<span data-ttu-id="19a8a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a8a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a8a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a8a-123">입력</span><span class="sxs-lookup"><span data-stu-id="19a8a-123">INPUTS</span></span>

## <span data-ttu-id="19a8a-124">출력</span><span class="sxs-lookup"><span data-stu-id="19a8a-124">OUTPUTS</span></span>

### <span data-ttu-id="19a8a-125">System.webserver. List ' 1 [SdkModels. t e m. m m Providerfeature]</span><span class="sxs-lookup"><span data-stu-id="19a8a-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="19a8a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="19a8a-126">NOTES</span></span>

## <span data-ttu-id="19a8a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19a8a-127">RELATED LINKS</span></span>

[<span data-ttu-id="19a8a-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="19a8a-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


