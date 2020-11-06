---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538188"
---
# <span data-ttu-id="da31c-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="da31c-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="da31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da31c-102">SYNOPSIS</span></span>
<span data-ttu-id="da31c-103">Azure Data Lake Store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da31c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da31c-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da31c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da31c-105">DESCRIPTION</span></span>
<span data-ttu-id="da31c-106">**AzureRmDataLakeStoreItemExpiry** Cmdlet은 Azure Data Lake store 계정에서 파일의 만료 시간을 설정 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="da31c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da31c-107">EXAMPLES</span></span>

### <span data-ttu-id="da31c-108">예제 1: 파일의 만료 시간 설정</span><span class="sxs-lookup"><span data-stu-id="da31c-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="da31c-109">계정 ContosoADL의 파일 myfile.txt에서 만료를 2 시간으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="da31c-110">이렇게 하면 두 시간 후에 파일이 만료 됩니다 (삭제 하도록 표시 됨).</span><span class="sxs-lookup"><span data-stu-id="da31c-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="da31c-111">예제 2: 파일에서 만료 제거</span><span class="sxs-lookup"><span data-stu-id="da31c-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="da31c-112">' ContosoADL ' 계정에서 ' myfile.txt ' 파일에 대해 이전에 설정 된 만료를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="da31c-113">즉, 파일이 자동으로 만료 (삭제로 표시 됨) 되며 수동으로 삭제 하거나 만료 되도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="da31c-114">변수</span><span class="sxs-lookup"><span data-stu-id="da31c-114">PARAMETERS</span></span>

### <span data-ttu-id="da31c-115">-계정</span><span class="sxs-lookup"><span data-stu-id="da31c-115">-Account</span></span>
<span data-ttu-id="da31c-116">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-116">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da31c-117">-만료</span><span class="sxs-lookup"><span data-stu-id="da31c-117">-Expiration</span></span>
<span data-ttu-id="da31c-118">지정 된 파일의 절대 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="da31c-119">값이 없거나 MaxValue로 설정 되어 있으면 파일이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da31c-120">-Path</span><span class="sxs-lookup"><span data-stu-id="da31c-120">-Path</span></span>
<span data-ttu-id="da31c-121">만료를 설정 하거나 제거할 파일 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da31c-122">-확인</span><span class="sxs-lookup"><span data-stu-id="da31c-122">-Confirm</span></span>
<span data-ttu-id="da31c-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da31c-124">-WhatIf</span></span>
<span data-ttu-id="da31c-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da31c-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da31c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da31c-127">-DefaultProfile</span></span>
<span data-ttu-id="da31c-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da31c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da31c-129">CommonParameters</span></span>
<span data-ttu-id="da31c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da31c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da31c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da31c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da31c-132">입력</span><span class="sxs-lookup"><span data-stu-id="da31c-132">INPUTS</span></span>

## <span data-ttu-id="da31c-133">출력</span><span class="sxs-lookup"><span data-stu-id="da31c-133">OUTPUTS</span></span>

### <span data-ttu-id="da31c-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da31c-134">DataLakeStoreItem</span></span>
<span data-ttu-id="da31c-135">새로운 만료 시간으로 업데이트 된 파일</span><span class="sxs-lookup"><span data-stu-id="da31c-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="da31c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="da31c-136">NOTES</span></span>
<span data-ttu-id="da31c-137">별칭: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="da31c-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="da31c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da31c-138">RELATED LINKS</span></span>

[<span data-ttu-id="da31c-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da31c-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

