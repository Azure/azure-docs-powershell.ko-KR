---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703594"
---
# <span data-ttu-id="cacff-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="cacff-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="cacff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cacff-102">SYNOPSIS</span></span>
<span data-ttu-id="cacff-103">그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cacff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cacff-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cacff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cacff-105">DESCRIPTION</span></span>
<span data-ttu-id="cacff-106">**추가-AzureRmApiManagementUserToGroup** cmdlet은 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="cacff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cacff-107">EXAMPLES</span></span>

### <span data-ttu-id="cacff-108">예제 1: 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="cacff-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="cacff-109">이 명령은 기존 그룹에 기존 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="cacff-110">변수</span><span class="sxs-lookup"><span data-stu-id="cacff-110">PARAMETERS</span></span>

### <span data-ttu-id="cacff-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cacff-111">-Context</span></span>
<span data-ttu-id="cacff-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cacff-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cacff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacff-114">-DefaultProfile</span></span>
<span data-ttu-id="cacff-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cacff-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="cacff-116">-GroupId</span></span>
<span data-ttu-id="cacff-117">그룹 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-117">Specifies the group ID.</span></span>
<span data-ttu-id="cacff-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cacff-119">-PassThru</span></span>
<span data-ttu-id="cacff-120">passthru</span><span class="sxs-lookup"><span data-stu-id="cacff-120">passthru</span></span>

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

### <span data-ttu-id="cacff-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="cacff-121">-UserId</span></span>
<span data-ttu-id="cacff-122">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-122">Specifies the user ID.</span></span>
<span data-ttu-id="cacff-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-123">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacff-124">CommonParameters</span></span>
<span data-ttu-id="cacff-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacff-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cacff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacff-127">입력</span><span class="sxs-lookup"><span data-stu-id="cacff-127">INPUTS</span></span>

### <span data-ttu-id="cacff-128">않아야</span><span class="sxs-lookup"><span data-stu-id="cacff-128">None</span></span>
<span data-ttu-id="cacff-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cacff-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cacff-130">출력</span><span class="sxs-lookup"><span data-stu-id="cacff-130">OUTPUTS</span></span>

### <span data-ttu-id="cacff-131">나타내는</span><span class="sxs-lookup"><span data-stu-id="cacff-131">Boolean</span></span>

## <span data-ttu-id="cacff-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cacff-132">NOTES</span></span>

## <span data-ttu-id="cacff-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cacff-133">RELATED LINKS</span></span>

[<span data-ttu-id="cacff-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cacff-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="cacff-135">제거-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="cacff-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


