---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309325"
---
# <span data-ttu-id="2637c-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2637c-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="2637c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2637c-102">SYNOPSIS</span></span>
<span data-ttu-id="2637c-103">지정 된 응용 프로그램에 대 한 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="2637c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2637c-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2637c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2637c-105">DESCRIPTION</span></span>
<span data-ttu-id="2637c-106">**AzBatchApplication** cmdlet은 지정 된 Azure Batch application에 대 한 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="2637c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2637c-107">EXAMPLES</span></span>

### <span data-ttu-id="2637c-108">예제 1: 일괄 처리 계정에서 응용 프로그램 업데이트</span><span class="sxs-lookup"><span data-stu-id="2637c-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="2637c-109">이 명령은 ContosoBatch 계정의 Litware 응용 프로그램에서 업데이트를 허용 하는지 여부를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="2637c-110">이 명령은 응용 프로그램의 기본 버전 또는 표시 이름을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="2637c-111">변수</span><span class="sxs-lookup"><span data-stu-id="2637c-111">PARAMETERS</span></span>

### <span data-ttu-id="2637c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2637c-112">-AccountName</span></span>
<span data-ttu-id="2637c-113">이 cmdlet이 응용 프로그램을 수정 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="2637c-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="2637c-114">-AllowUpdates</span></span>
<span data-ttu-id="2637c-115">동일한 버전 문자열을 사용 하 여 응용 프로그램 내에서 패키지를 덮어쓸 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="2637c-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2637c-116">-ApplicationName</span></span>
<span data-ttu-id="2637c-117">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2637c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2637c-118">-DefaultProfile</span></span>
<span data-ttu-id="2637c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2637c-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="2637c-120">-DefaultVersion</span></span>
<span data-ttu-id="2637c-121">클라이언트가 응용 프로그램을 요청 하지만 버전을 지정 하지 않은 경우 사용할 패키지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="2637c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2637c-122">-DisplayName</span></span>
<span data-ttu-id="2637c-123">응용 프로그램의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="2637c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2637c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2637c-125">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="2637c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2637c-126">CommonParameters</span></span>
<span data-ttu-id="2637c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2637c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2637c-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2637c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2637c-129">입력</span><span class="sxs-lookup"><span data-stu-id="2637c-129">INPUTS</span></span>

### <span data-ttu-id="2637c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2637c-130">System.String</span></span>

### <span data-ttu-id="2637c-131">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="2637c-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2637c-132">출력</span><span class="sxs-lookup"><span data-stu-id="2637c-132">OUTPUTS</span></span>

### <span data-ttu-id="2637c-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2637c-133">System.Void</span></span>

## <span data-ttu-id="2637c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2637c-134">NOTES</span></span>

## <span data-ttu-id="2637c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2637c-135">RELATED LINKS</span></span>

[<span data-ttu-id="2637c-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2637c-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="2637c-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2637c-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="2637c-138">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2637c-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="2637c-139">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2637c-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="2637c-140">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2637c-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="2637c-141">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2637c-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


