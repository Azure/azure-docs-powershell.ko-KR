---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698507"
---
# <span data-ttu-id="76fa1-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="76fa1-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="76fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="76fa1-103">Azure 저장소 Blob 서비스에 대 한 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76fa1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76fa1-104">SYNTAX</span></span>

### <span data-ttu-id="76fa1-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="76fa1-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76fa1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="76fa1-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fa1-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="76fa1-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76fa1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="76fa1-108">DESCRIPTION</span></span>
<span data-ttu-id="76fa1-109">**AzStorageBlobServiceProperty** Cmdlet은 Azure Storage Blob 서비스에 대 한 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76fa1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="76fa1-110">EXAMPLES</span></span>

### <span data-ttu-id="76fa1-111">예제 1: Blob service DefaultServiceVersion을 2018-03-28로 설정</span><span class="sxs-lookup"><span data-stu-id="76fa1-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="76fa1-112">이 명령은 DefaultServiceVersion Blob 서비스를 2018-03-28으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="76fa1-113">변수</span><span class="sxs-lookup"><span data-stu-id="76fa1-113">PARAMETERS</span></span>

### <span data-ttu-id="76fa1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fa1-114">-DefaultProfile</span></span>
<span data-ttu-id="76fa1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fa1-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="76fa1-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="76fa1-117">설정할 기본 서비스 버전</span><span class="sxs-lookup"><span data-stu-id="76fa1-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fa1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fa1-118">-ResourceGroupName</span></span>
<span data-ttu-id="76fa1-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="76fa1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76fa1-120">-ResourceId</span></span>
<span data-ttu-id="76fa1-121">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="76fa1-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="76fa1-122">-StorageAccount</span></span>
<span data-ttu-id="76fa1-123">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="76fa1-123">Storage account object</span></span>

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

### <span data-ttu-id="76fa1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="76fa1-124">-StorageAccountName</span></span>
<span data-ttu-id="76fa1-125">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="76fa1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="76fa1-126">-Confirm</span></span>
<span data-ttu-id="76fa1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fa1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fa1-128">-WhatIf</span></span>
<span data-ttu-id="76fa1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76fa1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fa1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fa1-131">CommonParameters</span></span>
<span data-ttu-id="76fa1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fa1-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76fa1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fa1-134">입력</span><span class="sxs-lookup"><span data-stu-id="76fa1-134">INPUTS</span></span>

### <span data-ttu-id="76fa1-135">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76fa1-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="76fa1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76fa1-136">System.String</span></span>

## <span data-ttu-id="76fa1-137">출력</span><span class="sxs-lookup"><span data-stu-id="76fa1-137">OUTPUTS</span></span>

### <span data-ttu-id="76fa1-138">Microsoft. a. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="76fa1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="76fa1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="76fa1-139">NOTES</span></span>

## <span data-ttu-id="76fa1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76fa1-140">RELATED LINKS</span></span>
