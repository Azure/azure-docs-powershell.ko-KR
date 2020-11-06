---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532980"
---
# <span data-ttu-id="81936-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="81936-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="81936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81936-102">SYNOPSIS</span></span>
<span data-ttu-id="81936-103">리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81936-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81936-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81936-104">SYNTAX</span></span>

### <span data-ttu-id="81936-105">ListAvailable (기본값)</span><span class="sxs-lookup"><span data-stu-id="81936-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81936-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="81936-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81936-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81936-107">DESCRIPTION</span></span>
<span data-ttu-id="81936-108">**Get-AzureRmResourceProvider** Cmdlet은 Azure 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81936-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="81936-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81936-109">EXAMPLES</span></span>

## <span data-ttu-id="81936-110">변수</span><span class="sxs-lookup"><span data-stu-id="81936-110">PARAMETERS</span></span>

### <span data-ttu-id="81936-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="81936-111">-ApiVersion</span></span>
<span data-ttu-id="81936-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81936-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="81936-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81936-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="81936-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="81936-114">-ListAvailable</span></span>
<span data-ttu-id="81936-115">이 작업에서 사용 가능한 모든 리소스 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81936-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="81936-116">-위치</span><span class="sxs-lookup"><span data-stu-id="81936-116">-Location</span></span>
<span data-ttu-id="81936-117">리소스 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81936-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="81936-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="81936-118">-Pre</span></span>
<span data-ttu-id="81936-119">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81936-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="81936-120">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="81936-120">-ProviderNamespace</span></span>
<span data-ttu-id="81936-121">리소스 공급자의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81936-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81936-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81936-122">-DefaultProfile</span></span>
<span data-ttu-id="81936-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81936-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81936-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81936-124">CommonParameters</span></span>
<span data-ttu-id="81936-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81936-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81936-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81936-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81936-127">입력</span><span class="sxs-lookup"><span data-stu-id="81936-127">INPUTS</span></span>

## <span data-ttu-id="81936-128">출력</span><span class="sxs-lookup"><span data-stu-id="81936-128">OUTPUTS</span></span>

### <span data-ttu-id="81936-129">SdkModels. PSResourceProvider에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="81936-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="81936-130">상속자</span><span class="sxs-lookup"><span data-stu-id="81936-130">NOTES</span></span>

## <span data-ttu-id="81936-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81936-131">RELATED LINKS</span></span>

[<span data-ttu-id="81936-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="81936-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="81936-133">등록 취소-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="81936-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


