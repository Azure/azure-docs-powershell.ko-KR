---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049256"
---
# <span data-ttu-id="68993-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="68993-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="68993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68993-102">SYNOPSIS</span></span>
<span data-ttu-id="68993-103">명명 된 특정 값의 비밀 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68993-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="68993-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68993-104">SYNTAX</span></span>

### <span data-ttu-id="68993-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="68993-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68993-106">Getbynamedeid</span><span class="sxs-lookup"><span data-stu-id="68993-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68993-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68993-107">DESCRIPTION</span></span>
<span data-ttu-id="68993-108">명명 된 특정 값의 비밀 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68993-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="68993-109">예제의</span><span class="sxs-lookup"><span data-stu-id="68993-109">EXAMPLES</span></span>

### <span data-ttu-id="68993-110">예제 1: 이름으로 명명 된 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="68993-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="68993-111">이 명령은 명명 된 값 이름이 지정 된 명명 된 값 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68993-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="68993-112">변수</span><span class="sxs-lookup"><span data-stu-id="68993-112">PARAMETERS</span></span>

### <span data-ttu-id="68993-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="68993-113">-Context</span></span>
<span data-ttu-id="68993-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="68993-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68993-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68993-115">This parameter is required.</span></span>

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

### <span data-ttu-id="68993-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68993-116">-DefaultProfile</span></span>
<span data-ttu-id="68993-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68993-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68993-118">-Named= Eid</span><span class="sxs-lookup"><span data-stu-id="68993-118">-NamedValueId</span></span>
<span data-ttu-id="68993-119">명명 된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68993-119">Identifier of a the named value.</span></span>
<span data-ttu-id="68993-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="68993-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68993-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68993-121">CommonParameters</span></span>
<span data-ttu-id="68993-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68993-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68993-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68993-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68993-124">입력</span><span class="sxs-lookup"><span data-stu-id="68993-124">INPUTS</span></span>

### <span data-ttu-id="68993-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68993-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68993-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68993-126">System.String</span></span>

## <span data-ttu-id="68993-127">출력</span><span class="sxs-lookup"><span data-stu-id="68993-127">OUTPUTS</span></span>

### <span data-ttu-id="68993-128">ApiManagement. ServiceManagement. \ PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="68993-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="68993-129">상속자</span><span class="sxs-lookup"><span data-stu-id="68993-129">NOTES</span></span>

## <span data-ttu-id="68993-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68993-130">RELATED LINKS</span></span>
