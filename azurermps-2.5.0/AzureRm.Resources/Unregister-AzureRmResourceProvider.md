---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ead0edddccc5372c04e2e4b77d7860bbad29c27a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881254"
---
# <span data-ttu-id="85c20-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85c20-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="85c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c20-102">SYNOPSIS</span></span>
<span data-ttu-id="85c20-103">리소스 공급자의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85c20-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85c20-105">DESCRIPTION</span></span>
<span data-ttu-id="85c20-106">AzureRmResourceProvider cmdlet은 Azure 리소스 공급자의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="85c20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="85c20-107">EXAMPLES</span></span>

## <span data-ttu-id="85c20-108">변수</span><span class="sxs-lookup"><span data-stu-id="85c20-108">PARAMETERS</span></span>

### <span data-ttu-id="85c20-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="85c20-109">-ApiVersion</span></span>
<span data-ttu-id="85c20-110">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="85c20-111">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="85c20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c20-112">-DefaultProfile</span></span>
<span data-ttu-id="85c20-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85c20-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c20-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="85c20-114">-Pre</span></span>
<span data-ttu-id="85c20-115">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="85c20-116">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="85c20-116">-ProviderNamespace</span></span>
<span data-ttu-id="85c20-117">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="85c20-118">-확인</span><span class="sxs-lookup"><span data-stu-id="85c20-118">-Confirm</span></span>
<span data-ttu-id="85c20-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c20-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c20-120">-WhatIf</span></span>
<span data-ttu-id="85c20-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c20-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c20-123">CommonParameters</span></span>
<span data-ttu-id="85c20-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85c20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c20-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c20-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c20-126">입력</span><span class="sxs-lookup"><span data-stu-id="85c20-126">INPUTS</span></span>

## <span data-ttu-id="85c20-127">출력</span><span class="sxs-lookup"><span data-stu-id="85c20-127">OUTPUTS</span></span>

## <span data-ttu-id="85c20-128">상속자</span><span class="sxs-lookup"><span data-stu-id="85c20-128">NOTES</span></span>

## <span data-ttu-id="85c20-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85c20-129">RELATED LINKS</span></span>

[<span data-ttu-id="85c20-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85c20-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="85c20-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="85c20-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


