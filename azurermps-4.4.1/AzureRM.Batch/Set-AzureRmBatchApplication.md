---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: c1170dc6413c615c7ea1941cc9a446fe2da1610b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531172"
---
# <span data-ttu-id="1a268-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1a268-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="1a268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a268-102">SYNOPSIS</span></span>
<span data-ttu-id="1a268-103">지정 된 응용 프로그램에 대 한 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a268-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a268-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a268-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a268-105">DESCRIPTION</span></span>
<span data-ttu-id="1a268-106">**AzureRmBatchApplication** cmdlet은 지정 된 Azure Batch application에 대 한 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="1a268-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a268-107">EXAMPLES</span></span>

### <span data-ttu-id="1a268-108">예제 1: 일괄 처리 계정에서 응용 프로그램 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a268-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="1a268-109">이 명령은 ContosoBatch 계정의 Llitware 응용 프로그램에서 업데이트를 허용 하는지 여부를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="1a268-110">이 명령은 응용 프로그램의 기본 버전 또는 표시 이름을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="1a268-111">변수</span><span class="sxs-lookup"><span data-stu-id="1a268-111">PARAMETERS</span></span>

### <span data-ttu-id="1a268-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a268-112">-AccountName</span></span>
<span data-ttu-id="1a268-113">이 cmdlet이 응용 프로그램을 수정 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="1a268-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="1a268-114">-AllowUpdates</span></span>
<span data-ttu-id="1a268-115">동일한 버전 문자열을 사용 하 여 응용 프로그램 내에서 패키지를 덮어쓸 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a268-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1a268-116">-ApplicationId</span></span>
<span data-ttu-id="1a268-117">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a268-118">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="1a268-118">-DefaultVersion</span></span>
<span data-ttu-id="1a268-119">클라이언트가 응용 프로그램을 요청 하지만 버전을 지정 하지 않은 경우 사용할 패키지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-119">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a268-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1a268-120">-DisplayName</span></span>
<span data-ttu-id="1a268-121">응용 프로그램의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a268-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a268-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a268-123">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-123">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a268-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a268-124">-DefaultProfile</span></span>
<span data-ttu-id="1a268-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a268-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a268-126">CommonParameters</span></span>
<span data-ttu-id="1a268-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a268-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a268-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a268-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a268-129">입력</span><span class="sxs-lookup"><span data-stu-id="1a268-129">INPUTS</span></span>

## <span data-ttu-id="1a268-130">출력</span><span class="sxs-lookup"><span data-stu-id="1a268-130">OUTPUTS</span></span>

## <span data-ttu-id="1a268-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1a268-131">NOTES</span></span>

## <span data-ttu-id="1a268-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a268-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a268-133">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1a268-133">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="1a268-134">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1a268-134">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1a268-135">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1a268-135">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="1a268-136">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1a268-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1a268-137">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1a268-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="1a268-138">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1a268-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

