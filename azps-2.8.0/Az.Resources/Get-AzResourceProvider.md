---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871838"
---
# <span data-ttu-id="da299-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="da299-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="da299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da299-102">SYNOPSIS</span></span>
<span data-ttu-id="da299-103">리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da299-103">Gets a resource provider.</span></span>

## <span data-ttu-id="da299-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da299-104">SYNTAX</span></span>

### <span data-ttu-id="da299-105">ListAvailable (기본값)</span><span class="sxs-lookup"><span data-stu-id="da299-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da299-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="da299-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da299-107">설명은</span><span class="sxs-lookup"><span data-stu-id="da299-107">DESCRIPTION</span></span>
<span data-ttu-id="da299-108">**Get-AzResourceProvider** Cmdlet은 Azure 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da299-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="da299-109">예제의</span><span class="sxs-lookup"><span data-stu-id="da299-109">EXAMPLES</span></span>

## <span data-ttu-id="da299-110">변수</span><span class="sxs-lookup"><span data-stu-id="da299-110">PARAMETERS</span></span>

### <span data-ttu-id="da299-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da299-111">-ApiVersion</span></span>
<span data-ttu-id="da299-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da299-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="da299-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da299-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="da299-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da299-114">-DefaultProfile</span></span>
<span data-ttu-id="da299-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="da299-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da299-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="da299-116">-ListAvailable</span></span>
<span data-ttu-id="da299-117">이 작업에서 사용 가능한 모든 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da299-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="da299-118">-위치</span><span class="sxs-lookup"><span data-stu-id="da299-118">-Location</span></span>
<span data-ttu-id="da299-119">리소스 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da299-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="da299-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="da299-120">-Pre</span></span>
<span data-ttu-id="da299-121">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da299-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da299-122">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="da299-122">-ProviderNamespace</span></span>
<span data-ttu-id="da299-123">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da299-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="da299-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da299-124">CommonParameters</span></span>
<span data-ttu-id="da299-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da299-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da299-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da299-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da299-127">입력</span><span class="sxs-lookup"><span data-stu-id="da299-127">INPUTS</span></span>

### <span data-ttu-id="da299-128">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="da299-128">System.String[]</span></span>

## <span data-ttu-id="da299-129">출력</span><span class="sxs-lookup"><span data-stu-id="da299-129">OUTPUTS</span></span>

### <span data-ttu-id="da299-130">SdkModels. PSResourceProvider에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="da299-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="da299-131">상속자</span><span class="sxs-lookup"><span data-stu-id="da299-131">NOTES</span></span>

## <span data-ttu-id="da299-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da299-132">RELATED LINKS</span></span>

[<span data-ttu-id="da299-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="da299-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="da299-134">등록 취소-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="da299-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


