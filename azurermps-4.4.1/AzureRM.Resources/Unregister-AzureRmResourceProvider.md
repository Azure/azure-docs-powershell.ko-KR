---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: 686e6902c7653f4a820f51b02b134a51963bb532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702693"
---
# <span data-ttu-id="d2a5f-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d2a5f-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="d2a5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a5f-103">리소스 공급자의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2a5f-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a5f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a5f-106">AzureRmResourceProvider cmdlet은 Azure 리소스 공급자의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="d2a5f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d2a5f-107">EXAMPLES</span></span>

## <span data-ttu-id="d2a5f-108">변수</span><span class="sxs-lookup"><span data-stu-id="d2a5f-108">PARAMETERS</span></span>

### <span data-ttu-id="d2a5f-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d2a5f-109">-ApiVersion</span></span>
<span data-ttu-id="d2a5f-110">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d2a5f-111">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d2a5f-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="d2a5f-112">-Pre</span></span>
<span data-ttu-id="d2a5f-113">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d2a5f-114">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d2a5f-114">-ProviderNamespace</span></span>
<span data-ttu-id="d2a5f-115">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="d2a5f-116">-확인</span><span class="sxs-lookup"><span data-stu-id="d2a5f-116">-Confirm</span></span>
<span data-ttu-id="d2a5f-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a5f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a5f-118">-WhatIf</span></span>
<span data-ttu-id="d2a5f-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a5f-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a5f-121">-DefaultProfile</span></span>
<span data-ttu-id="d2a5f-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a5f-123">CommonParameters</span></span>
<span data-ttu-id="d2a5f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a5f-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a5f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a5f-126">입력</span><span class="sxs-lookup"><span data-stu-id="d2a5f-126">INPUTS</span></span>

## <span data-ttu-id="d2a5f-127">출력</span><span class="sxs-lookup"><span data-stu-id="d2a5f-127">OUTPUTS</span></span>

### <span data-ttu-id="d2a5f-128">System.webserver. List ' 1 [SdkModels. t e PSResourceProvider]를 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2a5f-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider]</span></span>

## <span data-ttu-id="d2a5f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d2a5f-129">NOTES</span></span>

## <span data-ttu-id="d2a5f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2a5f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2a5f-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d2a5f-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="d2a5f-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d2a5f-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


