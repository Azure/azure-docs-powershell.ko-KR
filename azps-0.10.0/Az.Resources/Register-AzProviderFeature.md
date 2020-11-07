---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: b7c2be59ecf43c117a459d489af70dac7c836094
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876415"
---
# <span data-ttu-id="20417-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="20417-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="20417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20417-102">SYNOPSIS</span></span>
<span data-ttu-id="20417-103">계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="20417-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20417-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20417-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20417-105">DESCRIPTION</span></span>
<span data-ttu-id="20417-106">**AzProviderFeature** cmdlet은 계정에 Azure 공급자 기능을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="20417-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20417-107">EXAMPLES</span></span>

### <span data-ttu-id="20417-108">예제 1: 기능 등록</span><span class="sxs-lookup"><span data-stu-id="20417-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="20417-109">이렇게 하면 Microsoft. 네트워크에 대 한 AllowApplicationSecurityGroups 기능이 계정에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20417-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="20417-110">변수</span><span class="sxs-lookup"><span data-stu-id="20417-110">PARAMETERS</span></span>

### <span data-ttu-id="20417-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20417-111">-DefaultProfile</span></span>
<span data-ttu-id="20417-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20417-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20417-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="20417-113">-FeatureName</span></span>
<span data-ttu-id="20417-114">이 cmdlet이 등록 하는 기능의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="20417-115">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="20417-115">-ProviderNamespace</span></span>
<span data-ttu-id="20417-116">이 cmdlet이 공급자 기능을 등록할 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="20417-117">-확인</span><span class="sxs-lookup"><span data-stu-id="20417-117">-Confirm</span></span>
<span data-ttu-id="20417-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20417-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20417-119">-WhatIf</span></span>
<span data-ttu-id="20417-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20417-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20417-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20417-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20417-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20417-122">CommonParameters</span></span>
<span data-ttu-id="20417-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20417-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20417-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20417-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20417-125">입력</span><span class="sxs-lookup"><span data-stu-id="20417-125">INPUTS</span></span>

## <span data-ttu-id="20417-126">출력</span><span class="sxs-lookup"><span data-stu-id="20417-126">OUTPUTS</span></span>

## <span data-ttu-id="20417-127">상속자</span><span class="sxs-lookup"><span data-stu-id="20417-127">NOTES</span></span>

## <span data-ttu-id="20417-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20417-128">RELATED LINKS</span></span>

[<span data-ttu-id="20417-129">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="20417-129">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


