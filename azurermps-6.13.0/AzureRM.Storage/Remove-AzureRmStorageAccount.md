---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536491"
---
# <span data-ttu-id="d3cf2-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3cf2-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="d3cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cf2-103">Azure에서 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3cf2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3cf2-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3cf2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3cf2-106">**AzureRmStorageAccount** Cmdlet은 Azure에서 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d3cf2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3cf2-107">EXAMPLES</span></span>

### <span data-ttu-id="d3cf2-108">예제 1: 저장소 계정 제거</span><span class="sxs-lookup"><span data-stu-id="d3cf2-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d3cf2-109">이 명령은 지정 된 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="d3cf2-110">변수</span><span class="sxs-lookup"><span data-stu-id="d3cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="d3cf2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3cf2-111">-AsJob</span></span>
<span data-ttu-id="d3cf2-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3cf2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3cf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3cf2-113">-DefaultProfile</span></span>
<span data-ttu-id="d3cf2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3cf2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3cf2-115">-Force</span></span>
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

### <span data-ttu-id="d3cf2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="d3cf2-116">-Name</span></span>
<span data-ttu-id="d3cf2-117">제거할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="d3cf2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3cf2-118">-ResourceGroupName</span></span>
<span data-ttu-id="d3cf2-119">제거할 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="d3cf2-120">-확인</span><span class="sxs-lookup"><span data-stu-id="d3cf2-120">-Confirm</span></span>
<span data-ttu-id="d3cf2-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3cf2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3cf2-122">-WhatIf</span></span>
<span data-ttu-id="d3cf2-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3cf2-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3cf2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cf2-125">CommonParameters</span></span>
<span data-ttu-id="d3cf2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3cf2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cf2-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3cf2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cf2-128">입력</span><span class="sxs-lookup"><span data-stu-id="d3cf2-128">INPUTS</span></span>

### <span data-ttu-id="d3cf2-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3cf2-129">System.String</span></span>

## <span data-ttu-id="d3cf2-130">출력</span><span class="sxs-lookup"><span data-stu-id="d3cf2-130">OUTPUTS</span></span>

### <span data-ttu-id="d3cf2-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d3cf2-131">System.Void</span></span>

## <span data-ttu-id="d3cf2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d3cf2-132">NOTES</span></span>

## <span data-ttu-id="d3cf2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3cf2-133">RELATED LINKS</span></span>

[<span data-ttu-id="d3cf2-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3cf2-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="d3cf2-135">새로운 AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3cf2-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="d3cf2-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3cf2-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


