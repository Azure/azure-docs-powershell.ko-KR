---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: f4ed396f1abbd8a123bb0e765e288c1ae55d25fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698337"
---
# <span data-ttu-id="0b0e6-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="0b0e6-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="0b0e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0e6-103">웹 앱에 탑재할 Azure 저장소 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="0b0e6-104">이 매개 변수는 Set-AzWebApp (-AzureStoragePath)로 사용 하기 위한 것입니다 Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0b0e6-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="0b0e6-105">구문과</span><span class="sxs-lookup"><span data-stu-id="0b0e6-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b0e6-106">설명은</span><span class="sxs-lookup"><span data-stu-id="0b0e6-106">DESCRIPTION</span></span>
<span data-ttu-id="0b0e6-107">웹 앱 내에 탑재할 Azure 저장소 경로를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="0b0e6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0b0e6-108">EXAMPLES</span></span>

### <span data-ttu-id="0b0e6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b0e6-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="0b0e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b0e6-110">PARAMETERS</span></span>

### <span data-ttu-id="0b0e6-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="0b0e6-111">-AccessKey</span></span>
<span data-ttu-id="0b0e6-112">Azure 저장소 계정에 대 한 선택 키</span><span class="sxs-lookup"><span data-stu-id="0b0e6-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b0e6-113">-AccountName</span></span>
<span data-ttu-id="0b0e6-114">Azure 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-114">Azure Storage account name.</span></span>
<span data-ttu-id="0b0e6-115">예: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="0b0e6-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0e6-116">-DefaultProfile</span></span>
<span data-ttu-id="0b0e6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0e6-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="0b0e6-118">-MountPath</span></span>
<span data-ttu-id="0b0e6-119">ShareName에 의해 지정 된 공유가 노출 되는 컨테이너의 경로</span><span class="sxs-lookup"><span data-stu-id="0b0e6-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0b0e6-120">-Name</span></span>
<span data-ttu-id="0b0e6-121">Azure Storage 속성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="0b0e6-122">웹 앱 또는 슬롯 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0b0e6-123">-ShareName</span></span>
<span data-ttu-id="0b0e6-124">컨테이너에 탑재할 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-125">-Type</span><span class="sxs-lookup"><span data-stu-id="0b0e6-125">-Type</span></span>
<span data-ttu-id="0b0e6-126">Azure 저장소 계정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="0b0e6-127">Windows 컨테이너는 Azure 파일만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b0e6-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0b0e6-128">-Confirm</span></span>
<span data-ttu-id="0b0e6-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0e6-130">-WhatIf</span></span>
<span data-ttu-id="0b0e6-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b0e6-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0e6-133">CommonParameters</span></span>
<span data-ttu-id="0b0e6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0e6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b0e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0e6-136">입력</span><span class="sxs-lookup"><span data-stu-id="0b0e6-136">INPUTS</span></span>

### <span data-ttu-id="0b0e6-137">않아야</span><span class="sxs-lookup"><span data-stu-id="0b0e6-137">None</span></span>

## <span data-ttu-id="0b0e6-138">출력</span><span class="sxs-lookup"><span data-stu-id="0b0e6-138">OUTPUTS</span></span>

### <span data-ttu-id="0b0e6-139">WebAppAzureStoragePath를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b0e6-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="0b0e6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="0b0e6-140">NOTES</span></span>

## <span data-ttu-id="0b0e6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b0e6-141">RELATED LINKS</span></span>
