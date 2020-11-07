---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698095"
---
# <span data-ttu-id="10e57-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="10e57-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="10e57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e57-102">SYNOPSIS</span></span>
<span data-ttu-id="10e57-103">SSO 토큰과 API Management 서비스의 배포 된 관리 포털에 대 한 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="10e57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10e57-104">SYNTAX</span></span>

### <span data-ttu-id="10e57-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="10e57-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e57-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10e57-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10e57-107">설명은</span><span class="sxs-lookup"><span data-stu-id="10e57-107">DESCRIPTION</span></span>
<span data-ttu-id="10e57-108">**AzApiManagementSsoToken** CMDLET은 SSO (single sign-on) 토큰이 포함 된 링크 (URL)를 API management 서비스의 배포 된 관리 포털에 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="10e57-109">예제의</span><span class="sxs-lookup"><span data-stu-id="10e57-109">EXAMPLES</span></span>

### <span data-ttu-id="10e57-110">예제 1: API Management 서비스의 SSO 토큰 가져오기</span><span class="sxs-lookup"><span data-stu-id="10e57-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="10e57-111">이 명령은 API Management 서비스의 SSO 토큰을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="10e57-112">변수</span><span class="sxs-lookup"><span data-stu-id="10e57-112">PARAMETERS</span></span>

### <span data-ttu-id="10e57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e57-113">-DefaultProfile</span></span>
<span data-ttu-id="10e57-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e57-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10e57-115">-InputObject</span></span>
<span data-ttu-id="10e57-116">PsApiManagement의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="10e57-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10e57-118">-이름</span><span class="sxs-lookup"><span data-stu-id="10e57-118">-Name</span></span>
<span data-ttu-id="10e57-119">API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e57-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e57-120">-ResourceGroupName</span></span>
<span data-ttu-id="10e57-121">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e57-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e57-122">CommonParameters</span></span>
<span data-ttu-id="10e57-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10e57-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e57-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="10e57-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e57-125">입력</span><span class="sxs-lookup"><span data-stu-id="10e57-125">INPUTS</span></span>

### <span data-ttu-id="10e57-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10e57-126">System.String</span></span>

## <span data-ttu-id="10e57-127">출력</span><span class="sxs-lookup"><span data-stu-id="10e57-127">OUTPUTS</span></span>

### <span data-ttu-id="10e57-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10e57-128">System.String</span></span>

## <span data-ttu-id="10e57-129">상속자</span><span class="sxs-lookup"><span data-stu-id="10e57-129">NOTES</span></span>

## <span data-ttu-id="10e57-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10e57-130">RELATED LINKS</span></span>

[<span data-ttu-id="10e57-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="10e57-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


