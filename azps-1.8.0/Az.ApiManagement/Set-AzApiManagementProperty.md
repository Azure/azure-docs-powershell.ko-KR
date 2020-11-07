---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869322"
---
# <span data-ttu-id="1be7a-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be7a-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="1be7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be7a-102">SYNOPSIS</span></span>
<span data-ttu-id="1be7a-103">API Management 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="1be7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1be7a-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1be7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1be7a-105">DESCRIPTION</span></span>
<span data-ttu-id="1be7a-106">**AzApiManagementProperty** Cmdlet은 Azure API Management 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="1be7a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1be7a-107">EXAMPLES</span></span>

### <span data-ttu-id="1be7a-108">예제 1: 속성의 태그 변경</span><span class="sxs-lookup"><span data-stu-id="1be7a-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="1be7a-109">첫 번째 명령은 $Tags 변수에 두 개의 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="1be7a-110">두 번째 명령은 ID Property11를 가진 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="1be7a-111">명령은 $Tags의 문자열을 속성의 태그로 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="1be7a-112">예제 2: 비밀 값을 가질 수 있도록 속성 수정</span><span class="sxs-lookup"><span data-stu-id="1be7a-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="1be7a-113">이 명령은 암호화 된 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="1be7a-114">변수</span><span class="sxs-lookup"><span data-stu-id="1be7a-114">PARAMETERS</span></span>

### <span data-ttu-id="1be7a-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1be7a-115">-Context</span></span>
<span data-ttu-id="1be7a-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1be7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be7a-117">-DefaultProfile</span></span>
<span data-ttu-id="1be7a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1be7a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1be7a-119">-Name</span></span>
<span data-ttu-id="1be7a-120">속성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-120">Specifies the name of the property.</span></span>
<span data-ttu-id="1be7a-121">최대 길이는 100 자입니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="1be7a-122">이름에는 문자, 숫자, 마침표, 대시, 밑줄 문자만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="1be7a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1be7a-123">-PassThru</span></span>
<span data-ttu-id="1be7a-124">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementProperty** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1be7a-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="1be7a-125">-PropertyId</span></span>
<span data-ttu-id="1be7a-126">이 cmdlet이 수정 하는 속성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1be7a-127">-비밀</span><span class="sxs-lookup"><span data-stu-id="1be7a-127">-Secret</span></span>
<span data-ttu-id="1be7a-128">속성 값이 비밀 이며 암호화 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be7a-129">태그</span><span class="sxs-lookup"><span data-stu-id="1be7a-129">-Tag</span></span>
<span data-ttu-id="1be7a-130">속성과 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-130">Tags associated with a property.</span></span> <span data-ttu-id="1be7a-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="1be7a-132">-값</span><span class="sxs-lookup"><span data-stu-id="1be7a-132">-Value</span></span>
<span data-ttu-id="1be7a-133">속성에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-133">Specifies a value for the property.</span></span>
<span data-ttu-id="1be7a-134">이 값에는 정책 식이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="1be7a-135">최대 길이는 1000 자입니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="1be7a-136">값이 비어 있거나 공백으로만 구성 되어 있지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="1be7a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be7a-137">CommonParameters</span></span>
<span data-ttu-id="1be7a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be7a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be7a-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be7a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be7a-140">입력</span><span class="sxs-lookup"><span data-stu-id="1be7a-140">INPUTS</span></span>

### <span data-ttu-id="1be7a-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1be7a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1be7a-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1be7a-142">System.String</span></span>

### <span data-ttu-id="1be7a-143">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1be7a-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1be7a-144">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="1be7a-144">System.String[]</span></span>

### <span data-ttu-id="1be7a-145">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1be7a-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1be7a-146">출력</span><span class="sxs-lookup"><span data-stu-id="1be7a-146">OUTPUTS</span></span>

### <span data-ttu-id="1be7a-147">ApiManagement. ServiceManagement. \ PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be7a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="1be7a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="1be7a-148">NOTES</span></span>

## <span data-ttu-id="1be7a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1be7a-149">RELATED LINKS</span></span>

[<span data-ttu-id="1be7a-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be7a-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="1be7a-151">새로운 AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be7a-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="1be7a-152">제거-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be7a-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


