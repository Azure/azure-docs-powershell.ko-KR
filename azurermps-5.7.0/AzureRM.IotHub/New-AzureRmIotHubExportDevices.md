---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711169"
---
# <span data-ttu-id="1f37b-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="1f37b-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="1f37b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f37b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f37b-103">새 장치 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f37b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f37b-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f37b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f37b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f37b-106">IotHub에 대 한 새 기기 내보내기 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="1f37b-107">이렇게 하면 모든 장치가 지정 된 컨테이너로 내보내기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="1f37b-108">SAS URI를 생성 하는 방법에 대해서는 다음 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f37b-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="1f37b-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="1f37b-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="1f37b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1f37b-110">EXAMPLES</span></span>

### <span data-ttu-id="1f37b-111">예제 1에서는 내보내기 장치 요청을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="1f37b-112">키를 제외 하 고 IotHub "myiothub"에 대 한 새 내보내기 장치 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="1f37b-113">변수</span><span class="sxs-lookup"><span data-stu-id="1f37b-113">PARAMETERS</span></span>

### <span data-ttu-id="1f37b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f37b-114">-DefaultProfile</span></span>
<span data-ttu-id="1f37b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f37b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1f37b-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="1f37b-117">Blob을 내보낼 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="1f37b-118">-Name</span></span>
<span data-ttu-id="1f37b-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f37b-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f37b-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1f37b-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-122">-확인</span><span class="sxs-lookup"><span data-stu-id="1f37b-122">-Confirm</span></span>
<span data-ttu-id="1f37b-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f37b-124">-WhatIf</span></span>
<span data-ttu-id="1f37b-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f37b-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f37b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f37b-127">CommonParameters</span></span>
<span data-ttu-id="1f37b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f37b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f37b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f37b-130">입력</span><span class="sxs-lookup"><span data-stu-id="1f37b-130">INPUTS</span></span>

### <span data-ttu-id="1f37b-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f37b-131">System.String</span></span>

## <span data-ttu-id="1f37b-132">출력</span><span class="sxs-lookup"><span data-stu-id="1f37b-132">OUTPUTS</span></span>

### <span data-ttu-id="1f37b-133">IotHub의 JobResponse입니다.</span><span class="sxs-lookup"><span data-stu-id="1f37b-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="1f37b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="1f37b-134">NOTES</span></span>

## <span data-ttu-id="1f37b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f37b-135">RELATED LINKS</span></span>

