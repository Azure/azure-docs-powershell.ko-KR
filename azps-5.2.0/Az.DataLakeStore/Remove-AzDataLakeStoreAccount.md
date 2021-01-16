---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333098"
---
# <span data-ttu-id="bfe06-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bfe06-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="bfe06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe06-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe06-103">Data Lake Store 계정을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="bfe06-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfe06-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe06-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfe06-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe06-106">**Remove-AzDataLakeStoreAccount** cmdlet은 Data Lake Store 계정을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="bfe06-107">예제</span><span class="sxs-lookup"><span data-stu-id="bfe06-107">EXAMPLES</span></span>

### <span data-ttu-id="bfe06-108">예제 1: Data Lake Store 계정 제거</span><span class="sxs-lookup"><span data-stu-id="bfe06-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="bfe06-109">이 명령은 Data Lake Store에서 ContosoADL이라는 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="bfe06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfe06-110">PARAMETERS</span></span>

### <span data-ttu-id="bfe06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe06-111">-DefaultProfile</span></span>
<span data-ttu-id="bfe06-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bfe06-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfe06-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bfe06-113">-Force</span></span>
<span data-ttu-id="bfe06-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bfe06-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bfe06-115">-Name</span></span>
<span data-ttu-id="bfe06-116">제거할 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="bfe06-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe06-117">-PassThru</span></span>
<span data-ttu-id="bfe06-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bfe06-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bfe06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe06-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfe06-121">제거할 계정이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="bfe06-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfe06-122">-Confirm</span></span>
<span data-ttu-id="bfe06-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe06-124">-WhatIf</span></span>
<span data-ttu-id="bfe06-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bfe06-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe06-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe06-127">CommonParameters</span></span>
<span data-ttu-id="bfe06-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe06-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bfe06-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe06-130">입력</span><span class="sxs-lookup"><span data-stu-id="bfe06-130">INPUTS</span></span>

### <span data-ttu-id="bfe06-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bfe06-131">System.String</span></span>

## <span data-ttu-id="bfe06-132">출력</span><span class="sxs-lookup"><span data-stu-id="bfe06-132">OUTPUTS</span></span>

### <span data-ttu-id="bfe06-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfe06-133">System.Boolean</span></span>

## <span data-ttu-id="bfe06-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfe06-134">NOTES</span></span>

## <span data-ttu-id="bfe06-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfe06-135">RELATED LINKS</span></span>

[<span data-ttu-id="bfe06-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bfe06-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bfe06-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bfe06-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bfe06-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bfe06-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bfe06-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bfe06-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

