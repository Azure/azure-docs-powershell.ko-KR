---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056923"
---
# <span data-ttu-id="4542d-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="4542d-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="4542d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4542d-102">SYNOPSIS</span></span>
<span data-ttu-id="4542d-103">저장소 계정에서 Blob 복원 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="4542d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4542d-104">SYNTAX</span></span>

### <span data-ttu-id="4542d-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4542d-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4542d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4542d-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4542d-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="4542d-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4542d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4542d-108">DESCRIPTION</span></span>
<span data-ttu-id="4542d-109">**AzStorageBlobRestorePolicy** Cmdlet은 Azure Storage blob 서비스에 대 한 Blob Restore 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="4542d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4542d-110">EXAMPLES</span></span>

### <span data-ttu-id="4542d-111">예제 1: 저장소 계정에서 Azure Storage Blob 서비스에 대 한 Blob Restore 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="4542d-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="4542d-112">이 명령은 저장소 계정에서 Azure Storage Blob 서비스에 대 한 Blob Restore 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="4542d-113">변수</span><span class="sxs-lookup"><span data-stu-id="4542d-113">PARAMETERS</span></span>

### <span data-ttu-id="4542d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4542d-114">-DefaultProfile</span></span>
<span data-ttu-id="4542d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4542d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4542d-116">-PassThru</span></span>
<span data-ttu-id="4542d-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="4542d-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="4542d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4542d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4542d-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4542d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4542d-120">-ResourceId</span></span>
<span data-ttu-id="4542d-121">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4542d-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4542d-122">-StorageAccount</span></span>
<span data-ttu-id="4542d-123">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="4542d-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4542d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4542d-124">-StorageAccountName</span></span>
<span data-ttu-id="4542d-125">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4542d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="4542d-126">-Confirm</span></span>
<span data-ttu-id="4542d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4542d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4542d-128">-WhatIf</span></span>
<span data-ttu-id="4542d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4542d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4542d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4542d-131">CommonParameters</span></span>
<span data-ttu-id="4542d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4542d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4542d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4542d-134">입력</span><span class="sxs-lookup"><span data-stu-id="4542d-134">INPUTS</span></span>

### <span data-ttu-id="4542d-135">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4542d-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4542d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4542d-136">System.String</span></span>

## <span data-ttu-id="4542d-137">출력</span><span class="sxs-lookup"><span data-stu-id="4542d-137">OUTPUTS</span></span>

### <span data-ttu-id="4542d-138">PSRestorePolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4542d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="4542d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4542d-139">NOTES</span></span>

## <span data-ttu-id="4542d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4542d-140">RELATED LINKS</span></span>
