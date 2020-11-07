---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: d969dcc0906def107b68a76980b39482dfe8c4e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876237"
---
# <span data-ttu-id="53042-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53042-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="53042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53042-102">SYNOPSIS</span></span>
<span data-ttu-id="53042-103">Azure에서 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="53042-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53042-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53042-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53042-105">DESCRIPTION</span></span>
<span data-ttu-id="53042-106">**AzStorageAccount** Cmdlet은 Azure에서 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="53042-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53042-107">EXAMPLES</span></span>

### <span data-ttu-id="53042-108">예제 1: 저장소 계정 제거</span><span class="sxs-lookup"><span data-stu-id="53042-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="53042-109">이 명령은 지정 된 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="53042-110">변수</span><span class="sxs-lookup"><span data-stu-id="53042-110">PARAMETERS</span></span>

### <span data-ttu-id="53042-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53042-111">-AsJob</span></span>
<span data-ttu-id="53042-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53042-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53042-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53042-113">-DefaultProfile</span></span>
<span data-ttu-id="53042-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53042-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53042-115">-Force</span><span class="sxs-lookup"><span data-stu-id="53042-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53042-116">-이름</span><span class="sxs-lookup"><span data-stu-id="53042-116">-Name</span></span>
<span data-ttu-id="53042-117">제거할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53042-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53042-118">-ResourceGroupName</span></span>
<span data-ttu-id="53042-119">제거할 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="53042-120">-확인</span><span class="sxs-lookup"><span data-stu-id="53042-120">-Confirm</span></span>
<span data-ttu-id="53042-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53042-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53042-122">-WhatIf</span></span>
<span data-ttu-id="53042-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53042-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53042-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53042-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53042-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53042-125">CommonParameters</span></span>
<span data-ttu-id="53042-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53042-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53042-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53042-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53042-128">입력</span><span class="sxs-lookup"><span data-stu-id="53042-128">INPUTS</span></span>

### <span data-ttu-id="53042-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53042-129">System.String</span></span>

## <span data-ttu-id="53042-130">출력</span><span class="sxs-lookup"><span data-stu-id="53042-130">OUTPUTS</span></span>

### <span data-ttu-id="53042-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="53042-131">System.Void</span></span>

## <span data-ttu-id="53042-132">상속자</span><span class="sxs-lookup"><span data-stu-id="53042-132">NOTES</span></span>

## <span data-ttu-id="53042-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53042-133">RELATED LINKS</span></span>

[<span data-ttu-id="53042-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53042-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="53042-135">새로운 AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53042-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="53042-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53042-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


