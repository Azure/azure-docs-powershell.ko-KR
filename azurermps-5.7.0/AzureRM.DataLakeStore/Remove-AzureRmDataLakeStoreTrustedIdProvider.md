---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536811"
---
# <span data-ttu-id="0b3f6-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0b3f6-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0b3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3f6-103">지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b3f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b3f6-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b3f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="0b3f6-106">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0b3f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="0b3f6-108">예제 1: 신뢰할 수 있는 id 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="0b3f6-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="0b3f6-109">"ContosoADL" 계정에서 "MyProvider" 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="0b3f6-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="0b3f6-111">-계정</span><span class="sxs-lookup"><span data-stu-id="0b3f6-111">-Account</span></span>
<span data-ttu-id="0b3f6-112">신뢰할 수 있는 id 공급자를 제거 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="0b3f6-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3f6-113">-DefaultProfile</span></span>
<span data-ttu-id="0b3f6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0b3f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b3f6-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0b3f6-115">-Name</span></span>
<span data-ttu-id="0b3f6-116">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-116">The name of the trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b3f6-117">-PassThru</span></span>
<span data-ttu-id="0b3f6-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0b3f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b3f6-120">신뢰할 수 있는 id 공급자를 제거할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0b3f6-121">-Confirm</span></span>
<span data-ttu-id="0b3f6-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3f6-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3f6-124">CommonParameters</span></span>
<span data-ttu-id="0b3f6-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3f6-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3f6-127">입력</span><span class="sxs-lookup"><span data-stu-id="0b3f6-127">INPUTS</span></span>

### <span data-ttu-id="0b3f6-128">않아야</span><span class="sxs-lookup"><span data-stu-id="0b3f6-128">None</span></span>
<span data-ttu-id="0b3f6-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b3f6-130">출력</span><span class="sxs-lookup"><span data-stu-id="0b3f6-130">OUTPUTS</span></span>

### <span data-ttu-id="0b3f6-131">부울</span><span class="sxs-lookup"><span data-stu-id="0b3f6-131">bool</span></span>
<span data-ttu-id="0b3f6-132">PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3f6-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="0b3f6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0b3f6-133">NOTES</span></span>

## <span data-ttu-id="0b3f6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b3f6-134">RELATED LINKS</span></span>

