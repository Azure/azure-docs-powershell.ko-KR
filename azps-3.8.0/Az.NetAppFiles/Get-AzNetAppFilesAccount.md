---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: eb30f07e0443712e7287ae850f463070f5aca3f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877306"
---
# <span data-ttu-id="d16b4-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d16b4-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d16b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d16b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d16b4-103">ANF (Azure NetApp Files) 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d16b4-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="d16b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d16b4-104">SYNTAX</span></span>

### <span data-ttu-id="d16b4-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d16b4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d16b4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16b4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d16b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d16b4-107">DESCRIPTION</span></span>
<span data-ttu-id="d16b4-108">**Get-AzNetAppFilesAccount** cmdlet은 anf 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d16b4-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="d16b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d16b4-109">EXAMPLES</span></span>

### <span data-ttu-id="d16b4-110">예제 1: ANF 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="d16b4-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="d16b4-111">이 명령은 MyAnfAccount 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d16b4-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="d16b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="d16b4-112">PARAMETERS</span></span>

### <span data-ttu-id="d16b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16b4-113">-DefaultProfile</span></span>
<span data-ttu-id="d16b4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d16b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d16b4-115">-Name</span></span>
<span data-ttu-id="d16b4-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d16b4-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d16b4-118">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="d16b4-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16b4-119">-ResourceId</span></span>
<span data-ttu-id="d16b4-120">ANF 계정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="d16b4-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16b4-121">CommonParameters</span></span>
<span data-ttu-id="d16b4-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d16b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d16b4-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16b4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16b4-124">입력</span><span class="sxs-lookup"><span data-stu-id="d16b4-124">INPUTS</span></span>

### <span data-ttu-id="d16b4-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d16b4-125">System.String</span></span>

## <span data-ttu-id="d16b4-126">출력</span><span class="sxs-lookup"><span data-stu-id="d16b4-126">OUTPUTS</span></span>

### <span data-ttu-id="d16b4-127">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d16b4-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d16b4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d16b4-128">NOTES</span></span>

## <span data-ttu-id="d16b4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d16b4-129">RELATED LINKS</span></span>
