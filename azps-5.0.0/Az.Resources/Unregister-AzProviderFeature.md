---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218201"
---
# <span data-ttu-id="44592-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="44592-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="44592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44592-102">SYNOPSIS</span></span>
<span data-ttu-id="44592-103">계정에서 Azure 공급자 기능 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="44592-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="44592-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44592-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44592-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44592-105">DESCRIPTION</span></span>
<span data-ttu-id="44592-106">AzProviderFeature cmdlet은 계정에서 Azure 공급자 기능 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="44592-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="44592-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44592-107">EXAMPLES</span></span>

### <span data-ttu-id="44592-108">예제 1: 기능 등록 취소</span><span class="sxs-lookup"><span data-stu-id="44592-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="44592-109">이렇게 하면 계정에서 Microsoft AllowApplicationSecurityGroups 기능 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="44592-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="44592-110">변수</span><span class="sxs-lookup"><span data-stu-id="44592-110">PARAMETERS</span></span>

### <span data-ttu-id="44592-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44592-111">-DefaultProfile</span></span>
<span data-ttu-id="44592-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44592-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44592-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="44592-113">-FeatureName</span></span>
<span data-ttu-id="44592-114">기능 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44592-114">The feature name.</span></span>

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

### <span data-ttu-id="44592-115">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="44592-115">-ProviderNamespace</span></span>
<span data-ttu-id="44592-116">리소스 공급자 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="44592-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="44592-117">-확인</span><span class="sxs-lookup"><span data-stu-id="44592-117">-Confirm</span></span>
<span data-ttu-id="44592-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44592-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44592-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44592-119">-WhatIf</span></span>
<span data-ttu-id="44592-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44592-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44592-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44592-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44592-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44592-122">CommonParameters</span></span>
<span data-ttu-id="44592-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44592-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44592-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44592-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44592-125">입력</span><span class="sxs-lookup"><span data-stu-id="44592-125">INPUTS</span></span>

### <span data-ttu-id="44592-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44592-126">System.String</span></span>

## <span data-ttu-id="44592-127">출력</span><span class="sxs-lookup"><span data-stu-id="44592-127">OUTPUTS</span></span>

### <span data-ttu-id="44592-128">SdkModels PSProviderFeature. m m m 기능</span><span class="sxs-lookup"><span data-stu-id="44592-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="44592-129">상속자</span><span class="sxs-lookup"><span data-stu-id="44592-129">NOTES</span></span>

## <span data-ttu-id="44592-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44592-130">RELATED LINKS</span></span>