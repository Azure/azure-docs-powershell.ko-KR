---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042221"
---
# <span data-ttu-id="de32c-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="de32c-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="de32c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de32c-102">SYNOPSIS</span></span>
<span data-ttu-id="de32c-103">새 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-103">Creates a new Property.</span></span>

## <span data-ttu-id="de32c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de32c-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de32c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="de32c-105">DESCRIPTION</span></span>
<span data-ttu-id="de32c-106">**AzApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="de32c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="de32c-107">EXAMPLES</span></span>

### <span data-ttu-id="de32c-108">예제 1: 태그를 포함 하는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="de32c-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="de32c-109">첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="de32c-110">두 번째 명령에서는 속성을 만들고 $Tags 문자열을 속성의 태그로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="de32c-111">예제 2: 비밀 값이 있는 속성 만들기</span><span class="sxs-lookup"><span data-stu-id="de32c-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="de32c-112">이 명령은 암호화 된 값이 있는 **속성** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="de32c-113">변수</span><span class="sxs-lookup"><span data-stu-id="de32c-113">PARAMETERS</span></span>

### <span data-ttu-id="de32c-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="de32c-114">-Context</span></span>
<span data-ttu-id="de32c-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de32c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de32c-116">-DefaultProfile</span></span>
<span data-ttu-id="de32c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de32c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="de32c-118">-Name</span></span>
<span data-ttu-id="de32c-119">이 cmdlet이 만드는 속성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="de32c-120">최대 길이는 100 자입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="de32c-121">이름에는 문자, 숫자, 마침표, 대시, 밑줄 문자만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="de32c-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="de32c-122">-PropertyId</span></span>
<span data-ttu-id="de32c-123">속성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="de32c-124">최대 길이는 256 자입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="de32c-125">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="de32c-126">-비밀</span><span class="sxs-lookup"><span data-stu-id="de32c-126">-Secret</span></span>
<span data-ttu-id="de32c-127">속성 값이 비밀 이며 암호화 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="de32c-128">태그</span><span class="sxs-lookup"><span data-stu-id="de32c-128">-Tag</span></span>
<span data-ttu-id="de32c-129">속성과 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-129">Tags to be associated with Property.</span></span> <span data-ttu-id="de32c-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="de32c-131">-값</span><span class="sxs-lookup"><span data-stu-id="de32c-131">-Value</span></span>
<span data-ttu-id="de32c-132">속성에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-132">Specifies a value for the property.</span></span>
<span data-ttu-id="de32c-133">이 값에는 정책 식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="de32c-134">최대 길이는 1000 자입니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="de32c-135">값이 비어 있거나 공백으로만 구성 되어 있지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="de32c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de32c-136">CommonParameters</span></span>
<span data-ttu-id="de32c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de32c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de32c-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="de32c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de32c-139">입력</span><span class="sxs-lookup"><span data-stu-id="de32c-139">INPUTS</span></span>

### <span data-ttu-id="de32c-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="de32c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de32c-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de32c-141">System.String</span></span>

### <span data-ttu-id="de32c-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="de32c-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="de32c-143">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="de32c-143">System.String[]</span></span>

## <span data-ttu-id="de32c-144">출력</span><span class="sxs-lookup"><span data-stu-id="de32c-144">OUTPUTS</span></span>

### <span data-ttu-id="de32c-145">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="de32c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="de32c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="de32c-146">NOTES</span></span>

## <span data-ttu-id="de32c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de32c-147">RELATED LINKS</span></span>

[<span data-ttu-id="de32c-148">제거-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="de32c-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="de32c-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="de32c-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


