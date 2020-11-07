---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878333"
---
# <span data-ttu-id="096e2-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="096e2-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="096e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096e2-102">SYNOPSIS</span></span>
<span data-ttu-id="096e2-103">Data Lake Store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="096e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="096e2-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="096e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="096e2-105">DESCRIPTION</span></span>
<span data-ttu-id="096e2-106">**AzDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="096e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="096e2-107">EXAMPLES</span></span>

### <span data-ttu-id="096e2-108">예제 1: Data Lake Store 계정 제거</span><span class="sxs-lookup"><span data-stu-id="096e2-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="096e2-109">이 명령은 Data Lake Store에서 ContosoADL 이라는 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="096e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="096e2-110">PARAMETERS</span></span>

### <span data-ttu-id="096e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096e2-111">-DefaultProfile</span></span>
<span data-ttu-id="096e2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="096e2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="096e2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="096e2-113">-Force</span></span>
<span data-ttu-id="096e2-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="096e2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="096e2-115">-Name</span></span>
<span data-ttu-id="096e2-116">제거할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="096e2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="096e2-117">-PassThru</span></span>
<span data-ttu-id="096e2-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="096e2-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="096e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="096e2-121">제거할 계정이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="096e2-122">-확인</span><span class="sxs-lookup"><span data-stu-id="096e2-122">-Confirm</span></span>
<span data-ttu-id="096e2-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096e2-124">-WhatIf</span></span>
<span data-ttu-id="096e2-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="096e2-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096e2-127">CommonParameters</span></span>
<span data-ttu-id="096e2-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="096e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096e2-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096e2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096e2-130">입력</span><span class="sxs-lookup"><span data-stu-id="096e2-130">INPUTS</span></span>

### <span data-ttu-id="096e2-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="096e2-131">System.String</span></span>

## <span data-ttu-id="096e2-132">출력</span><span class="sxs-lookup"><span data-stu-id="096e2-132">OUTPUTS</span></span>

### <span data-ttu-id="096e2-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="096e2-133">System.Boolean</span></span>

## <span data-ttu-id="096e2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="096e2-134">NOTES</span></span>

## <span data-ttu-id="096e2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="096e2-135">RELATED LINKS</span></span>

[<span data-ttu-id="096e2-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="096e2-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="096e2-137">새로운 AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="096e2-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="096e2-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="096e2-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="096e2-139">테스트-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="096e2-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


