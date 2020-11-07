---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880610"
---
# <span data-ttu-id="0e964-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e964-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="0e964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e964-102">SYNOPSIS</span></span>
<span data-ttu-id="0e964-103">리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e964-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e964-104">SYNTAX</span></span>

### <span data-ttu-id="0e964-105">ListAvailable (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e964-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e964-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="0e964-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e964-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e964-107">DESCRIPTION</span></span>
<span data-ttu-id="0e964-108">**Get-AzureRmResourceProvider** Cmdlet은 Azure 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="0e964-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0e964-109">EXAMPLES</span></span>

## <span data-ttu-id="0e964-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e964-110">PARAMETERS</span></span>

### <span data-ttu-id="0e964-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e964-111">-ApiVersion</span></span>
<span data-ttu-id="0e964-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0e964-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0e964-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e964-114">-DefaultProfile</span></span>
<span data-ttu-id="0e964-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e964-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e964-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0e964-116">-ListAvailable</span></span>
<span data-ttu-id="0e964-117">이 작업에서 사용 가능한 모든 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e964-118">-위치</span><span class="sxs-lookup"><span data-stu-id="0e964-118">-Location</span></span>
<span data-ttu-id="0e964-119">리소스 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="0e964-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="0e964-120">-Pre</span></span>
<span data-ttu-id="0e964-121">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0e964-122">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0e964-122">-ProviderNamespace</span></span>
<span data-ttu-id="0e964-123">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e964-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e964-124">CommonParameters</span></span>
<span data-ttu-id="0e964-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e964-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e964-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e964-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e964-127">입력</span><span class="sxs-lookup"><span data-stu-id="0e964-127">INPUTS</span></span>

## <span data-ttu-id="0e964-128">출력</span><span class="sxs-lookup"><span data-stu-id="0e964-128">OUTPUTS</span></span>

## <span data-ttu-id="0e964-129">상속자</span><span class="sxs-lookup"><span data-stu-id="0e964-129">NOTES</span></span>

## <span data-ttu-id="0e964-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e964-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e964-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e964-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="0e964-132">등록 취소-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e964-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


