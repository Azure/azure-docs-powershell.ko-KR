---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489176"
---
# <span data-ttu-id="edc9c-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="edc9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="edc9c-103">Data Lake Store 계정의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="edc9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="edc9c-104">SYNTAX</span></span>

### <span data-ttu-id="edc9c-105">GetAllInSubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="edc9c-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edc9c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edc9c-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edc9c-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edc9c-108">설명</span><span class="sxs-lookup"><span data-stu-id="edc9c-108">DESCRIPTION</span></span>
<span data-ttu-id="edc9c-109">**Get-AzDataLakeStoreAccount** cmdlet은 Data Lake Store 계정의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="edc9c-110">예제</span><span class="sxs-lookup"><span data-stu-id="edc9c-110">EXAMPLES</span></span>

### <span data-ttu-id="edc9c-111">예제 1: Data Lake Store 계정 다운로드</span><span class="sxs-lookup"><span data-stu-id="edc9c-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="edc9c-112">이 명령은 ContosoADL이라는 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="edc9c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edc9c-113">PARAMETERS</span></span>

### <span data-ttu-id="edc9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc9c-114">-DefaultProfile</span></span>
<span data-ttu-id="edc9c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="edc9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edc9c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="edc9c-116">-Name</span></span>
<span data-ttu-id="edc9c-117">얻을 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc9c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc9c-118">-ResourceGroupName</span></span>
<span data-ttu-id="edc9c-119">얻을 Data Lake Store 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc9c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc9c-120">CommonParameters</span></span>
<span data-ttu-id="edc9c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edc9c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc9c-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="edc9c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc9c-123">입력</span><span class="sxs-lookup"><span data-stu-id="edc9c-123">INPUTS</span></span>

### <span data-ttu-id="edc9c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="edc9c-124">System.String</span></span>

## <span data-ttu-id="edc9c-125">출력</span><span class="sxs-lookup"><span data-stu-id="edc9c-125">OUTPUTS</span></span>

### <span data-ttu-id="edc9c-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="edc9c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edc9c-127">NOTES</span></span>

## <span data-ttu-id="edc9c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edc9c-128">RELATED LINKS</span></span>

[<span data-ttu-id="edc9c-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="edc9c-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="edc9c-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="edc9c-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edc9c-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


