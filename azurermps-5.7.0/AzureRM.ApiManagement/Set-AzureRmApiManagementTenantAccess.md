---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 55158ac4f6489d70e17008c9e8c4ef13bd6d4fe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711452"
---
# <span data-ttu-id="9a6a2-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9a6a2-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="9a6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6a2-103">테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a6a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a6a2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a6a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="9a6a2-106">**AzureRmApiManagementTenantAccess** cmdlet은 테 넌 트 액세스를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="9a6a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="9a6a2-108">예제 1: 테 넌 트 액세스 사용</span><span class="sxs-lookup"><span data-stu-id="9a6a2-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="9a6a2-109">이 명령은 지정 된 컨텍스트에서 테 넌 트 액세스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="9a6a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="9a6a2-110">PARAMETERS</span></span>

### <span data-ttu-id="9a6a2-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9a6a2-111">-Context</span></span>
<span data-ttu-id="9a6a2-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9a6a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6a2-113">-DefaultProfile</span></span>
<span data-ttu-id="9a6a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9a6a2-115">-사용</span><span class="sxs-lookup"><span data-stu-id="9a6a2-115">-Enabled</span></span>
<span data-ttu-id="9a6a2-116">이 cmdlet이 테 넌 트 액세스를 사용할지 또는 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="9a6a2-117">사용 하거나 사용 하지 않을 $False $True 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6a2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a6a2-118">-PassThru</span></span>
<span data-ttu-id="9a6a2-119">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementAccessInformation** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9a6a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6a2-120">CommonParameters</span></span>
<span data-ttu-id="9a6a2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6a2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6a2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6a2-123">입력</span><span class="sxs-lookup"><span data-stu-id="9a6a2-123">INPUTS</span></span>

### <span data-ttu-id="9a6a2-124">않아야</span><span class="sxs-lookup"><span data-stu-id="9a6a2-124">None</span></span>
<span data-ttu-id="9a6a2-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a6a2-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a6a2-126">출력</span><span class="sxs-lookup"><span data-stu-id="9a6a2-126">OUTPUTS</span></span>

### <span data-ttu-id="9a6a2-127">ApiManagement. ServiceManagement. \ PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9a6a2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9a6a2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9a6a2-128">NOTES</span></span>

## <span data-ttu-id="9a6a2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a6a2-129">RELATED LINKS</span></span>

[<span data-ttu-id="9a6a2-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9a6a2-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


