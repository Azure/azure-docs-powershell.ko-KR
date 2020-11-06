---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538080"
---
# <span data-ttu-id="29aa4-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="29aa4-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="29aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="29aa4-103">그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29aa4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29aa4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29aa4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="29aa4-106">**Remove-AzureRmApiManagementUserFromGroup** cmdlet은 기존 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="29aa4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="29aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="29aa4-108">예제 1: 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="29aa4-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="29aa4-109">이 명령은 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="29aa4-110">변수</span><span class="sxs-lookup"><span data-stu-id="29aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="29aa4-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="29aa4-111">-Context</span></span>
<span data-ttu-id="29aa4-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="29aa4-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="29aa4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29aa4-114">-DefaultProfile</span></span>
<span data-ttu-id="29aa4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="29aa4-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="29aa4-116">-GroupId</span></span>
<span data-ttu-id="29aa4-117">사용자를 제거할 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="29aa4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29aa4-118">-PassThru</span></span>
<span data-ttu-id="29aa4-119">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="29aa4-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="29aa4-120">-UserId</span></span>
<span data-ttu-id="29aa4-121">그룹에서 제거할 사용자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="29aa4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29aa4-122">CommonParameters</span></span>
<span data-ttu-id="29aa4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29aa4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29aa4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29aa4-125">입력</span><span class="sxs-lookup"><span data-stu-id="29aa4-125">INPUTS</span></span>

### <span data-ttu-id="29aa4-126">않아야</span><span class="sxs-lookup"><span data-stu-id="29aa4-126">None</span></span>
<span data-ttu-id="29aa4-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29aa4-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29aa4-128">출력</span><span class="sxs-lookup"><span data-stu-id="29aa4-128">OUTPUTS</span></span>

### <span data-ttu-id="29aa4-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="29aa4-129">System.Boolean</span></span>

## <span data-ttu-id="29aa4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="29aa4-130">NOTES</span></span>

## <span data-ttu-id="29aa4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29aa4-131">RELATED LINKS</span></span>

[<span data-ttu-id="29aa4-132">추가-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="29aa4-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="29aa4-133">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="29aa4-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


