---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882474"
---
# <span data-ttu-id="05b80-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="05b80-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="05b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b80-102">SYNOPSIS</span></span>
<span data-ttu-id="05b80-103">계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05b80-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="05b80-105">DESCRIPTION</span></span>
<span data-ttu-id="05b80-106">**AzureRmProviderFeature** cmdlet은 계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="05b80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="05b80-107">EXAMPLES</span></span>

### <span data-ttu-id="05b80-108">예제 1: 기능 등록</span><span class="sxs-lookup"><span data-stu-id="05b80-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="05b80-109">이렇게 하면 Microsoft. 네트워크에 대 한 AllowApplicationSecurityGroups 기능이 계정에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="05b80-110">변수</span><span class="sxs-lookup"><span data-stu-id="05b80-110">PARAMETERS</span></span>

### <span data-ttu-id="05b80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b80-111">-DefaultProfile</span></span>
<span data-ttu-id="05b80-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="05b80-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05b80-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="05b80-113">-FeatureName</span></span>
<span data-ttu-id="05b80-114">이 cmdlet이 등록 하는 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="05b80-115">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="05b80-115">-ProviderNamespace</span></span>
<span data-ttu-id="05b80-116">이 cmdlet이 공급자 기능을 등록할 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="05b80-117">-확인</span><span class="sxs-lookup"><span data-stu-id="05b80-117">-Confirm</span></span>
<span data-ttu-id="05b80-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b80-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b80-119">-WhatIf</span></span>
<span data-ttu-id="05b80-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b80-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b80-122">CommonParameters</span></span>
<span data-ttu-id="05b80-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b80-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b80-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b80-125">입력</span><span class="sxs-lookup"><span data-stu-id="05b80-125">INPUTS</span></span>

## <span data-ttu-id="05b80-126">출력</span><span class="sxs-lookup"><span data-stu-id="05b80-126">OUTPUTS</span></span>

## <span data-ttu-id="05b80-127">상속자</span><span class="sxs-lookup"><span data-stu-id="05b80-127">NOTES</span></span>

## <span data-ttu-id="05b80-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05b80-128">RELATED LINKS</span></span>

[<span data-ttu-id="05b80-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="05b80-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


