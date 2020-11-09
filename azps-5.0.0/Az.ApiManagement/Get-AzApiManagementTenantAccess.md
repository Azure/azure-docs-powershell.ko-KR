---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309353"
---
# <span data-ttu-id="25009-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="25009-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="25009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25009-102">SYNOPSIS</span></span>
<span data-ttu-id="25009-103">테 넌 트에 대 한 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25009-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="25009-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25009-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25009-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25009-105">DESCRIPTION</span></span>
<span data-ttu-id="25009-106">**AzApiManagementTenantAccess** cmdlet은 테 넌 트에 대 한 테 넌 트 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25009-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="25009-107">키가 결과 세부 정보에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25009-107">Keys will not be included into result details.</span></span> <span data-ttu-id="25009-108">클라이언트 비밀을 가져오려면 Get-help를 **AzApiManagementTenantAccessSecret** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25009-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="25009-109">예제의</span><span class="sxs-lookup"><span data-stu-id="25009-109">EXAMPLES</span></span>

### <span data-ttu-id="25009-110">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="25009-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="25009-111">이 명령은 지정 된 컨텍스트에 대 한 테 넌 트 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="25009-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="25009-112">변수</span><span class="sxs-lookup"><span data-stu-id="25009-112">PARAMETERS</span></span>

### <span data-ttu-id="25009-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="25009-113">-Context</span></span>
<span data-ttu-id="25009-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25009-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="25009-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25009-115">-DefaultProfile</span></span>
<span data-ttu-id="25009-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25009-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25009-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25009-117">CommonParameters</span></span>
<span data-ttu-id="25009-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25009-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25009-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25009-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25009-120">입력</span><span class="sxs-lookup"><span data-stu-id="25009-120">INPUTS</span></span>

### <span data-ttu-id="25009-121">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25009-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="25009-122">출력</span><span class="sxs-lookup"><span data-stu-id="25009-122">OUTPUTS</span></span>

### <span data-ttu-id="25009-123">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="25009-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="25009-124">상속자</span><span class="sxs-lookup"><span data-stu-id="25009-124">NOTES</span></span>

## <span data-ttu-id="25009-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25009-125">RELATED LINKS</span></span>

[<span data-ttu-id="25009-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="25009-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


