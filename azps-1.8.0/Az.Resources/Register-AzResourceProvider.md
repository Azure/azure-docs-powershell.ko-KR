---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 11ff763dacc5a6969501dae925fbbc2382c871b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699368"
---
# <span data-ttu-id="4851b-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4851b-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="4851b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4851b-102">SYNOPSIS</span></span>
<span data-ttu-id="4851b-103">리소스 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-103">Registers a resource provider.</span></span>

## <span data-ttu-id="4851b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4851b-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4851b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4851b-105">DESCRIPTION</span></span>
<span data-ttu-id="4851b-106">**AzResourceProvider** Cmdlet은 Azure 리소스 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="4851b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4851b-107">EXAMPLES</span></span>

### <span data-ttu-id="4851b-108">예제 1: 공급자 등록</span><span class="sxs-lookup"><span data-stu-id="4851b-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="4851b-109">계정에 대 한 Microsoft 네트워크 공급자를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="4851b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4851b-110">PARAMETERS</span></span>

### <span data-ttu-id="4851b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4851b-111">-ApiVersion</span></span>
<span data-ttu-id="4851b-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4851b-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4851b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4851b-114">-DefaultProfile</span></span>
<span data-ttu-id="4851b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4851b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4851b-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="4851b-116">-Pre</span></span>
<span data-ttu-id="4851b-117">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4851b-118">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4851b-118">-ProviderNamespace</span></span>
<span data-ttu-id="4851b-119">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="4851b-120">-확인</span><span class="sxs-lookup"><span data-stu-id="4851b-120">-Confirm</span></span>
<span data-ttu-id="4851b-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4851b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4851b-122">-WhatIf</span></span>
<span data-ttu-id="4851b-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4851b-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4851b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4851b-125">CommonParameters</span></span>
<span data-ttu-id="4851b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4851b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4851b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4851b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4851b-128">입력</span><span class="sxs-lookup"><span data-stu-id="4851b-128">INPUTS</span></span>

### <span data-ttu-id="4851b-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4851b-129">System.String</span></span>

## <span data-ttu-id="4851b-130">출력</span><span class="sxs-lookup"><span data-stu-id="4851b-130">OUTPUTS</span></span>

### <span data-ttu-id="4851b-131">SdkModels. PSResourceProvider에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="4851b-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="4851b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4851b-132">NOTES</span></span>

## <span data-ttu-id="4851b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4851b-133">RELATED LINKS</span></span>

[<span data-ttu-id="4851b-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4851b-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="4851b-135">등록 취소-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4851b-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


