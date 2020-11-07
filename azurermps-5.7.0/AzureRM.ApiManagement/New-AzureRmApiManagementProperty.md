---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711849"
---
# <span data-ttu-id="5b5dc-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5b5dc-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="5b5dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b5dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5dc-103">새 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b5dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b5dc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b5dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b5dc-105">DESCRIPTION</span></span>
<span data-ttu-id="5b5dc-106">**AzureRmApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="5b5dc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b5dc-107">EXAMPLES</span></span>

### <span data-ttu-id="5b5dc-108">예제 1: 태그를 포함 하는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="5b5dc-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="5b5dc-109">첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="5b5dc-110">두 번째 명령에서는 속성을 만들고 $Tags 문자열을 속성의 태그로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="5b5dc-111">예제 2: 비밀 값이 있는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="5b5dc-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="5b5dc-112">이 명령은 암호화 된 값이 있는 **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="5b5dc-113">변수</span><span class="sxs-lookup"><span data-stu-id="5b5dc-113">PARAMETERS</span></span>

### <span data-ttu-id="5b5dc-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5b5dc-114">-Context</span></span>
<span data-ttu-id="5b5dc-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5dc-116">-DefaultProfile</span></span>
<span data-ttu-id="5b5dc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5dc-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5b5dc-118">-Name</span></span>
<span data-ttu-id="5b5dc-119">이 cmdlet이 만드는 속성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="5b5dc-120">최대 길이는 100 자입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="5b5dc-121">이름에는 문자, 숫자, 마침표, 대시, 밑줄 문자만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="5b5dc-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="5b5dc-122">-PropertyId</span></span>
<span data-ttu-id="5b5dc-123">속성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="5b5dc-124">최대 길이는 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="5b5dc-125">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-125">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5dc-126">-비밀</span><span class="sxs-lookup"><span data-stu-id="5b5dc-126">-Secret</span></span>
<span data-ttu-id="5b5dc-127">속성 값이 비밀 이며 암호화 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5dc-128">태그</span><span class="sxs-lookup"><span data-stu-id="5b5dc-128">-Tag</span></span>
<span data-ttu-id="5b5dc-129">속성과 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-129">Tags to be associated with Property.</span></span> <span data-ttu-id="5b5dc-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-130">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5dc-131">-값</span><span class="sxs-lookup"><span data-stu-id="5b5dc-131">-Value</span></span>
<span data-ttu-id="5b5dc-132">속성에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-132">Specifies a value for the property.</span></span>
<span data-ttu-id="5b5dc-133">이 값에는 정책 식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="5b5dc-134">최대 길이는 1000 자입니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="5b5dc-135">값이 비어 있거나 공백으로만 구성 되어 있지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="5b5dc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5dc-136">CommonParameters</span></span>
<span data-ttu-id="5b5dc-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5dc-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b5dc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5dc-139">입력</span><span class="sxs-lookup"><span data-stu-id="5b5dc-139">INPUTS</span></span>

### <span data-ttu-id="5b5dc-140">않아야</span><span class="sxs-lookup"><span data-stu-id="5b5dc-140">None</span></span>
<span data-ttu-id="5b5dc-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b5dc-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b5dc-142">출력</span><span class="sxs-lookup"><span data-stu-id="5b5dc-142">OUTPUTS</span></span>

### <span data-ttu-id="5b5dc-143">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5b5dc-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="5b5dc-144">상속자</span><span class="sxs-lookup"><span data-stu-id="5b5dc-144">NOTES</span></span>

## <span data-ttu-id="5b5dc-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b5dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="5b5dc-146">제거-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5b5dc-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="5b5dc-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="5b5dc-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


