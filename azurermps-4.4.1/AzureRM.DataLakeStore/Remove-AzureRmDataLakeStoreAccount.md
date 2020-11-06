---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533091"
---
# <span data-ttu-id="ba871-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ba871-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="ba871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba871-102">SYNOPSIS</span></span>
<span data-ttu-id="ba871-103">Data Lake Store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba871-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba871-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba871-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba871-105">DESCRIPTION</span></span>
<span data-ttu-id="ba871-106">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="ba871-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba871-107">EXAMPLES</span></span>

### <span data-ttu-id="ba871-108">예제 1: Data Lake Store 계정 제거</span><span class="sxs-lookup"><span data-stu-id="ba871-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="ba871-109">이 명령은 Data Lake Store에서 ContosoADL 이라는 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="ba871-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba871-110">PARAMETERS</span></span>

### <span data-ttu-id="ba871-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ba871-111">-Force</span></span>
<span data-ttu-id="ba871-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ba871-113">-Name</span></span>
<span data-ttu-id="ba871-114">제거할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-114">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba871-115">-PassThru</span></span>
<span data-ttu-id="ba871-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba871-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba871-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba871-119">제거할 계정이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-119">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ba871-120">-Confirm</span></span>
<span data-ttu-id="ba871-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba871-122">-WhatIf</span></span>
<span data-ttu-id="ba871-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba871-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba871-125">-DefaultProfile</span></span>
<span data-ttu-id="ba871-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba871-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba871-127">CommonParameters</span></span>
<span data-ttu-id="ba871-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba871-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba871-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba871-130">입력</span><span class="sxs-lookup"><span data-stu-id="ba871-130">INPUTS</span></span>

## <span data-ttu-id="ba871-131">출력</span><span class="sxs-lookup"><span data-stu-id="ba871-131">OUTPUTS</span></span>

### <span data-ttu-id="ba871-132">부울</span><span class="sxs-lookup"><span data-stu-id="ba871-132">bool</span></span>
<span data-ttu-id="ba871-133">PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba871-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="ba871-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ba871-134">NOTES</span></span>

## <span data-ttu-id="ba871-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba871-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba871-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ba871-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ba871-137">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ba871-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ba871-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ba871-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ba871-139">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ba871-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


