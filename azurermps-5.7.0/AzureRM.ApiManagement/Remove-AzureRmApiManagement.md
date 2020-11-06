---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536139"
---
# <span data-ttu-id="24033-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="24033-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="24033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24033-102">SYNOPSIS</span></span>
<span data-ttu-id="24033-103">API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24033-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24033-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24033-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24033-105">DESCRIPTION</span></span>
<span data-ttu-id="24033-106">**AzureRmApiManagement** Cmdlet은 Azure API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="24033-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24033-107">EXAMPLES</span></span>

### <span data-ttu-id="24033-108">예제 1: API Management 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="24033-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="24033-109">이 명령은 ContosoApi 이라는 API Management 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="24033-110">변수</span><span class="sxs-lookup"><span data-stu-id="24033-110">PARAMETERS</span></span>

### <span data-ttu-id="24033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24033-111">-DefaultProfile</span></span>
<span data-ttu-id="24033-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24033-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="24033-113">-이름</span><span class="sxs-lookup"><span data-stu-id="24033-113">-Name</span></span>
<span data-ttu-id="24033-114">이 cmdlet이 제거 하는 API 관리 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="24033-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24033-115">-PassThru</span></span>
<span data-ttu-id="24033-116">작업이 성공할 경우이 cmdlet이 $True 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="24033-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24033-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24033-117">-ResourceGroupName</span></span>
<span data-ttu-id="24033-118">API Management 배포가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="24033-119">-확인</span><span class="sxs-lookup"><span data-stu-id="24033-119">-Confirm</span></span>
<span data-ttu-id="24033-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24033-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24033-121">-WhatIf</span></span>
<span data-ttu-id="24033-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24033-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24033-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24033-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24033-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24033-124">CommonParameters</span></span>
<span data-ttu-id="24033-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24033-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24033-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24033-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24033-127">입력</span><span class="sxs-lookup"><span data-stu-id="24033-127">INPUTS</span></span>

### <span data-ttu-id="24033-128">않아야</span><span class="sxs-lookup"><span data-stu-id="24033-128">None</span></span>
<span data-ttu-id="24033-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24033-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24033-130">출력</span><span class="sxs-lookup"><span data-stu-id="24033-130">OUTPUTS</span></span>

### <span data-ttu-id="24033-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="24033-131">System.Boolean</span></span>

## <span data-ttu-id="24033-132">상속자</span><span class="sxs-lookup"><span data-stu-id="24033-132">NOTES</span></span>

## <span data-ttu-id="24033-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24033-133">RELATED LINKS</span></span>

[<span data-ttu-id="24033-134">백업-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="24033-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="24033-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="24033-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="24033-136">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="24033-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="24033-137">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="24033-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


