---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489047"
---
# <span data-ttu-id="24e23-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24e23-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="24e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e23-102">SYNOPSIS</span></span>
<span data-ttu-id="24e23-103">Data Lake Store 계정의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="24e23-104">구문</span><span class="sxs-lookup"><span data-stu-id="24e23-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24e23-105">설명</span><span class="sxs-lookup"><span data-stu-id="24e23-105">DESCRIPTION</span></span>
<span data-ttu-id="24e23-106">**Test-AzDataLakeStoreAccount** cmdlet은 Data Lake Store 계정의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="24e23-107">예제</span><span class="sxs-lookup"><span data-stu-id="24e23-107">EXAMPLES</span></span>

### <span data-ttu-id="24e23-108">예제 1: 계정 테스트</span><span class="sxs-lookup"><span data-stu-id="24e23-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="24e23-109">이 명령은 ContosoADL이라는 계정이 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="24e23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24e23-110">PARAMETERS</span></span>

### <span data-ttu-id="24e23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e23-111">-DefaultProfile</span></span>
<span data-ttu-id="24e23-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24e23-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24e23-113">-Name</span><span class="sxs-lookup"><span data-stu-id="24e23-113">-Name</span></span>
<span data-ttu-id="24e23-114">테스트할 Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="24e23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e23-115">-ResourceGroupName</span></span>
<span data-ttu-id="24e23-116">테스트할 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="24e23-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e23-117">CommonParameters</span></span>
<span data-ttu-id="24e23-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24e23-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e23-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="24e23-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e23-120">입력</span><span class="sxs-lookup"><span data-stu-id="24e23-120">INPUTS</span></span>

### <span data-ttu-id="24e23-121">System.String</span><span class="sxs-lookup"><span data-stu-id="24e23-121">System.String</span></span>

## <span data-ttu-id="24e23-122">출력</span><span class="sxs-lookup"><span data-stu-id="24e23-122">OUTPUTS</span></span>

### <span data-ttu-id="24e23-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24e23-123">System.Boolean</span></span>

## <span data-ttu-id="24e23-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24e23-124">NOTES</span></span>

## <span data-ttu-id="24e23-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24e23-125">RELATED LINKS</span></span>

[<span data-ttu-id="24e23-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24e23-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="24e23-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24e23-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="24e23-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24e23-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="24e23-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="24e23-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


