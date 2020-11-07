---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701675"
---
# <span data-ttu-id="945b6-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="945b6-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="945b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="945b6-102">SYNOPSIS</span></span>
<span data-ttu-id="945b6-103">PsAzureApiManagementContext의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="945b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="945b6-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="945b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="945b6-105">DESCRIPTION</span></span>
<span data-ttu-id="945b6-106">**AzApiManagementContext** Cmdlet은 **PsAzureApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="945b6-107">컨텍스트는 모든 API Management 서비스 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="945b6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="945b6-108">EXAMPLES</span></span>

### <span data-ttu-id="945b6-109">예제 1: PsApiManagementContext 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="945b6-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="945b6-110">이 명령은 **PsApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="945b6-111">변수</span><span class="sxs-lookup"><span data-stu-id="945b6-111">PARAMETERS</span></span>

### <span data-ttu-id="945b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945b6-112">-DefaultProfile</span></span>
<span data-ttu-id="945b6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="945b6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945b6-114">-ResourceGroupName</span></span>
<span data-ttu-id="945b6-115">API Management 서비스를 배포 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="945b6-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="945b6-116">-ServiceName</span></span>
<span data-ttu-id="945b6-117">배포 된 API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="945b6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945b6-118">CommonParameters</span></span>
<span data-ttu-id="945b6-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="945b6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945b6-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945b6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945b6-121">입력</span><span class="sxs-lookup"><span data-stu-id="945b6-121">INPUTS</span></span>

### <span data-ttu-id="945b6-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="945b6-122">System.String</span></span>

## <span data-ttu-id="945b6-123">출력</span><span class="sxs-lookup"><span data-stu-id="945b6-123">OUTPUTS</span></span>

### <span data-ttu-id="945b6-124">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="945b6-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="945b6-125">상속자</span><span class="sxs-lookup"><span data-stu-id="945b6-125">NOTES</span></span>

## <span data-ttu-id="945b6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="945b6-126">RELATED LINKS</span></span>
