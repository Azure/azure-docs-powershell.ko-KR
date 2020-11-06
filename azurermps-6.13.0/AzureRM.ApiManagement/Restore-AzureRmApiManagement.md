---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 1fc22563949f44882d0b6ed1f864d217faacff9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533468"
---
# <span data-ttu-id="ec236-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec236-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="ec236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec236-102">SYNOPSIS</span></span>
<span data-ttu-id="ec236-103">지정 된 Azure storage blob에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec236-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec236-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec236-105">DESCRIPTION</span></span>
<span data-ttu-id="ec236-106">**AzureRmApiManagement** Cmdlet은 azurestorage blob에 상주 하는 지정 된 백업에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="ec236-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec236-107">EXAMPLES</span></span>

### <span data-ttu-id="ec236-108">예제 1: API Management 서비스 복원</span><span class="sxs-lookup"><span data-stu-id="ec236-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="ec236-109">이 명령은 Azure storage blob에서 API Management 서비스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="ec236-110">변수</span><span class="sxs-lookup"><span data-stu-id="ec236-110">PARAMETERS</span></span>

### <span data-ttu-id="ec236-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec236-111">-DefaultProfile</span></span>
<span data-ttu-id="ec236-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec236-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ec236-113">-Name</span></span>
<span data-ttu-id="ec236-114">백업과 함께 복원 될 API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec236-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec236-115">-PassThru</span></span>
<span data-ttu-id="ec236-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec236-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec236-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec236-118">-ResourceGroupName</span></span>
<span data-ttu-id="ec236-119">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec236-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="ec236-120">-SourceBlobName</span></span>
<span data-ttu-id="ec236-121">Azure 저장소 백업 원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec236-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="ec236-122">-SourceContainerName</span></span>
<span data-ttu-id="ec236-123">Azure 저장소 백업 원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec236-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ec236-124">-StorageContext</span></span>
<span data-ttu-id="ec236-125">저장소 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec236-126">CommonParameters</span></span>
<span data-ttu-id="ec236-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec236-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec236-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec236-129">입력</span><span class="sxs-lookup"><span data-stu-id="ec236-129">INPUTS</span></span>

### <span data-ttu-id="ec236-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec236-130">System.String</span></span>

## <span data-ttu-id="ec236-131">출력</span><span class="sxs-lookup"><span data-stu-id="ec236-131">OUTPUTS</span></span>

### <span data-ttu-id="ec236-132">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="ec236-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ec236-133">상속자</span><span class="sxs-lookup"><span data-stu-id="ec236-133">NOTES</span></span>

## <span data-ttu-id="ec236-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec236-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec236-135">백업-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec236-135">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="ec236-136">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec236-136">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ec236-137">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec236-137">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ec236-138">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ec236-138">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


