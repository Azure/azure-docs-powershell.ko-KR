---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 8fe856b1b8b710c1db139474f15d432f32c2652a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982251"
---
# <span data-ttu-id="e2777-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e2777-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="e2777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2777-102">SYNOPSIS</span></span>
<span data-ttu-id="e2777-103">리소스 공급자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-103">Registers a resource provider.</span></span>

## <span data-ttu-id="e2777-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2777-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2777-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2777-105">DESCRIPTION</span></span>
<span data-ttu-id="e2777-106">**Register-AzResourceProvider** cmdlet은 Azure 리소스 공급자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="e2777-107">예제</span><span class="sxs-lookup"><span data-stu-id="e2777-107">EXAMPLES</span></span>

### <span data-ttu-id="e2777-108">예제 1: 공급자 등록</span><span class="sxs-lookup"><span data-stu-id="e2777-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e2777-109">계정에 대해 Microsoft.Network 공급자를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="e2777-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2777-110">PARAMETERS</span></span>

### <span data-ttu-id="e2777-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2777-111">-ApiVersion</span></span>
<span data-ttu-id="e2777-112">리소스 공급자에서 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e2777-113">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e2777-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2777-114">-DefaultProfile</span></span>
<span data-ttu-id="e2777-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2777-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2777-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2777-116">-Pre</span></span>
<span data-ttu-id="e2777-117">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2777-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e2777-118">-ProviderNamespace</span></span>
<span data-ttu-id="e2777-119">리소스 공급자의 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e2777-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e2777-120">-Confirm</span></span>
<span data-ttu-id="e2777-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2777-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2777-122">-WhatIf</span></span>
<span data-ttu-id="e2777-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2777-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2777-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2777-125">CommonParameters</span></span>
<span data-ttu-id="e2777-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2777-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2777-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2777-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2777-128">입력</span><span class="sxs-lookup"><span data-stu-id="e2777-128">INPUTS</span></span>

### <span data-ttu-id="e2777-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e2777-129">System.String</span></span>

## <span data-ttu-id="e2777-130">출력</span><span class="sxs-lookup"><span data-stu-id="e2777-130">OUTPUTS</span></span>

### <span data-ttu-id="e2777-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e2777-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e2777-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2777-132">NOTES</span></span>

## <span data-ttu-id="e2777-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2777-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2777-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e2777-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e2777-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e2777-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


