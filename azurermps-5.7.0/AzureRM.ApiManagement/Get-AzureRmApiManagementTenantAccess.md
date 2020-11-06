---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 64f341398ff20f3eddf67c88c51a93125904d566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529963"
---
# <span data-ttu-id="dddee-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="dddee-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="dddee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dddee-102">SYNOPSIS</span></span>
<span data-ttu-id="dddee-103">테 넌 트에 대 한 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dddee-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dddee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dddee-105">DESCRIPTION</span></span>
<span data-ttu-id="dddee-106">**AzureRmApiManagementTenantAccess** cmdlet은 테 넌 트에 대 한 테 넌 트 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="dddee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dddee-107">EXAMPLES</span></span>

### <span data-ttu-id="dddee-108">예제 1: 테 넌 트 액세스 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="dddee-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext 
```

<span data-ttu-id="dddee-109">이 명령은 지정 된 컨텍스트에 대 한 테 넌 트 액세스 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="dddee-110">변수</span><span class="sxs-lookup"><span data-stu-id="dddee-110">PARAMETERS</span></span>

### <span data-ttu-id="dddee-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dddee-111">-Context</span></span>
<span data-ttu-id="dddee-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dddee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddee-113">-DefaultProfile</span></span>
<span data-ttu-id="dddee-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="dddee-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddee-115">CommonParameters</span></span>
<span data-ttu-id="dddee-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddee-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddee-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddee-118">입력</span><span class="sxs-lookup"><span data-stu-id="dddee-118">INPUTS</span></span>

### <span data-ttu-id="dddee-119">않아야</span><span class="sxs-lookup"><span data-stu-id="dddee-119">None</span></span>
<span data-ttu-id="dddee-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dddee-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dddee-121">출력</span><span class="sxs-lookup"><span data-stu-id="dddee-121">OUTPUTS</span></span>

### <span data-ttu-id="dddee-122">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="dddee-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="dddee-123">상속자</span><span class="sxs-lookup"><span data-stu-id="dddee-123">NOTES</span></span>

## <span data-ttu-id="dddee-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dddee-124">RELATED LINKS</span></span>

[<span data-ttu-id="dddee-125">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="dddee-125">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


