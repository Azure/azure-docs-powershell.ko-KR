---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526836"
---
# <span data-ttu-id="e7d50-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7d50-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="e7d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d50-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d50-103">Data Lake Store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7d50-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7d50-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d50-106">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e7d50-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7d50-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d50-108">예제 1: Data Lake Store 계정 제거</span><span class="sxs-lookup"><span data-stu-id="e7d50-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e7d50-109">이 명령은 Data Lake Store에서 ContosoADL 이라는 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="e7d50-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7d50-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d50-111">-DefaultProfile</span></span>
<span data-ttu-id="e7d50-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e7d50-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7d50-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d50-113">-Force</span></span>
<span data-ttu-id="e7d50-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e7d50-115">-Name</span></span>
<span data-ttu-id="e7d50-116">제거할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7d50-117">-PassThru</span></span>
<span data-ttu-id="e7d50-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7d50-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d50-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7d50-121">제거할 계정이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="e7d50-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e7d50-122">-Confirm</span></span>
<span data-ttu-id="e7d50-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d50-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d50-124">-WhatIf</span></span>
<span data-ttu-id="e7d50-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d50-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d50-127">CommonParameters</span></span>
<span data-ttu-id="e7d50-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d50-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d50-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d50-130">입력</span><span class="sxs-lookup"><span data-stu-id="e7d50-130">INPUTS</span></span>

### <span data-ttu-id="e7d50-131">않아야</span><span class="sxs-lookup"><span data-stu-id="e7d50-131">None</span></span>
<span data-ttu-id="e7d50-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7d50-133">출력</span><span class="sxs-lookup"><span data-stu-id="e7d50-133">OUTPUTS</span></span>

### <span data-ttu-id="e7d50-134">부울</span><span class="sxs-lookup"><span data-stu-id="e7d50-134">bool</span></span>
<span data-ttu-id="e7d50-135">PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d50-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="e7d50-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e7d50-136">NOTES</span></span>

## <span data-ttu-id="e7d50-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7d50-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7d50-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7d50-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e7d50-139">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7d50-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e7d50-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7d50-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e7d50-141">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e7d50-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


