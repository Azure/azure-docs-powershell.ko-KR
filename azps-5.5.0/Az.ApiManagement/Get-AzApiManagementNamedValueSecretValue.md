---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205728"
---
# <span data-ttu-id="74ca5-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="74ca5-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="74ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="74ca5-103">특정 명명된 값의 비밀 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="74ca5-104">구문</span><span class="sxs-lookup"><span data-stu-id="74ca5-104">SYNTAX</span></span>

### <span data-ttu-id="74ca5-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="74ca5-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74ca5-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="74ca5-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ca5-107">설명</span><span class="sxs-lookup"><span data-stu-id="74ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="74ca5-108">특정 명명된 값의 비밀 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="74ca5-109">예제</span><span class="sxs-lookup"><span data-stu-id="74ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="74ca5-110">예제 1: 이름으로 명명된 값 얻기</span><span class="sxs-lookup"><span data-stu-id="74ca5-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="74ca5-111">이 명령은 명명된 값 이름을 지정하는 명명된 값 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="74ca5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74ca5-112">PARAMETERS</span></span>

### <span data-ttu-id="74ca5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="74ca5-113">-Context</span></span>
<span data-ttu-id="74ca5-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="74ca5-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="74ca5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ca5-116">-DefaultProfile</span></span>
<span data-ttu-id="74ca5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74ca5-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="74ca5-118">-NamedValueId</span></span>
<span data-ttu-id="74ca5-119">명명된 값의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-119">Identifier of a the named value.</span></span>
<span data-ttu-id="74ca5-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-120">This parameter is required.</span></span>

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

### <span data-ttu-id="74ca5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ca5-121">CommonParameters</span></span>
<span data-ttu-id="74ca5-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74ca5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ca5-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74ca5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ca5-124">입력</span><span class="sxs-lookup"><span data-stu-id="74ca5-124">INPUTS</span></span>

### <span data-ttu-id="74ca5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="74ca5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74ca5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="74ca5-126">System.String</span></span>

## <span data-ttu-id="74ca5-127">출력</span><span class="sxs-lookup"><span data-stu-id="74ca5-127">OUTPUTS</span></span>

### <span data-ttu-id="74ca5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="74ca5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="74ca5-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74ca5-129">NOTES</span></span>

## <span data-ttu-id="74ca5-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74ca5-130">RELATED LINKS</span></span>
