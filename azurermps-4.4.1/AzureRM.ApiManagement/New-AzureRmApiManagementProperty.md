---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711003"
---
# <span data-ttu-id="a8e56-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a8e56-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="a8e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8e56-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e56-103">새 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8e56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8e56-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8e56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8e56-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e56-106">**AzureRmApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="a8e56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8e56-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e56-108">예제 1: 태그를 포함 하는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="a8e56-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="a8e56-109">첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="a8e56-110">두 번째 명령에서는 속성을 만들고 $Tags 문자열을 속성의 태그로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="a8e56-111">예제 2: 비밀 값이 있는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="a8e56-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="a8e56-112">이 명령은 암호화 된 값이 있는 **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="a8e56-113">변수</span><span class="sxs-lookup"><span data-stu-id="a8e56-113">PARAMETERS</span></span>

### <span data-ttu-id="a8e56-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a8e56-114">-Context</span></span>
<span data-ttu-id="a8e56-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e56-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a8e56-116">-Name</span></span>
<span data-ttu-id="a8e56-117">이 cmdlet이 만드는 속성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="a8e56-118">최대 길이는 100 자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="a8e56-119">이름에는 문자, 숫자, 마침표, 대시, 밑줄 문자만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="a8e56-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="a8e56-120">-PropertyId</span></span>
<span data-ttu-id="a8e56-121">속성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="a8e56-122">최대 길이는 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="a8e56-123">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-123">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e56-124">-비밀</span><span class="sxs-lookup"><span data-stu-id="a8e56-124">-Secret</span></span>
<span data-ttu-id="a8e56-125">속성 값이 비밀 이며 암호화 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-125">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e56-126">태그</span><span class="sxs-lookup"><span data-stu-id="a8e56-126">-Tags</span></span>
<span data-ttu-id="a8e56-127">이 cmdlet이 속성에 연결 하는 태그의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="a8e56-128">태그를 사용 하 여 속성 목록을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-128">You can use tags to filter the property list.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e56-129">-값</span><span class="sxs-lookup"><span data-stu-id="a8e56-129">-Value</span></span>
<span data-ttu-id="a8e56-130">속성에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-130">Specifies a value for the property.</span></span>
<span data-ttu-id="a8e56-131">이 값에는 정책 식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="a8e56-132">최대 길이는 1000 자입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="a8e56-133">값이 비어 있거나 공백으로만 구성 되어 있지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="a8e56-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e56-134">-DefaultProfile</span></span>
<span data-ttu-id="a8e56-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8e56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e56-136">CommonParameters</span></span>
<span data-ttu-id="a8e56-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e56-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e56-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e56-139">입력</span><span class="sxs-lookup"><span data-stu-id="a8e56-139">INPUTS</span></span>

## <span data-ttu-id="a8e56-140">출력</span><span class="sxs-lookup"><span data-stu-id="a8e56-140">OUTPUTS</span></span>

### <span data-ttu-id="a8e56-141">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a8e56-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="a8e56-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a8e56-142">NOTES</span></span>

## <span data-ttu-id="a8e56-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8e56-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8e56-144">제거-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a8e56-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="a8e56-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="a8e56-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


