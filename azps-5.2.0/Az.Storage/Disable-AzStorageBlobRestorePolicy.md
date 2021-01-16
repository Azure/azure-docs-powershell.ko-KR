---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349845"
---
# <span data-ttu-id="66481-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="66481-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="66481-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66481-102">SYNOPSIS</span></span>
<span data-ttu-id="66481-103">Storage 계정에서 Blob 복원 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="66481-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="66481-104">구문</span><span class="sxs-lookup"><span data-stu-id="66481-104">SYNTAX</span></span>

### <span data-ttu-id="66481-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="66481-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66481-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="66481-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66481-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="66481-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66481-108">설명</span><span class="sxs-lookup"><span data-stu-id="66481-108">DESCRIPTION</span></span>
<span data-ttu-id="66481-109">**Disable-AzStorageBlobRestorePolicy** cmdlet은 Azure Storage Blob 서비스에 대한 Blob 복원 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="66481-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="66481-110">예제</span><span class="sxs-lookup"><span data-stu-id="66481-110">EXAMPLES</span></span>

### <span data-ttu-id="66481-111">예제 1: Storage 계정에서 Azure Storage Blob service에 대한 Blob 복원 정책을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="66481-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="66481-112">이 명령은 Storage 계정의 Azure Storage Blob service에 대한 Blob 복원 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="66481-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="66481-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66481-113">PARAMETERS</span></span>

### <span data-ttu-id="66481-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66481-114">-DefaultProfile</span></span>
<span data-ttu-id="66481-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66481-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66481-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66481-116">-PassThru</span></span>
<span data-ttu-id="66481-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="66481-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="66481-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66481-118">-ResourceGroupName</span></span>
<span data-ttu-id="66481-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66481-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="66481-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66481-120">-ResourceId</span></span>
<span data-ttu-id="66481-121">Storage 계정 리소스 ID 또는 Blob service 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="66481-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="66481-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="66481-122">-StorageAccount</span></span>
<span data-ttu-id="66481-123">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="66481-123">Storage account object</span></span>

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

### <span data-ttu-id="66481-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="66481-124">-StorageAccountName</span></span>
<span data-ttu-id="66481-125">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66481-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="66481-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66481-126">-Confirm</span></span>
<span data-ttu-id="66481-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66481-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66481-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66481-128">-WhatIf</span></span>
<span data-ttu-id="66481-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="66481-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66481-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66481-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66481-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66481-131">CommonParameters</span></span>
<span data-ttu-id="66481-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66481-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66481-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66481-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66481-134">입력</span><span class="sxs-lookup"><span data-stu-id="66481-134">INPUTS</span></span>

### <span data-ttu-id="66481-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66481-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="66481-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66481-136">System.String</span></span>

## <span data-ttu-id="66481-137">출력</span><span class="sxs-lookup"><span data-stu-id="66481-137">OUTPUTS</span></span>

### <span data-ttu-id="66481-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="66481-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="66481-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66481-139">NOTES</span></span>

## <span data-ttu-id="66481-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66481-140">RELATED LINKS</span></span>
